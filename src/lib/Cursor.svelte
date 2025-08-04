<script lang="ts">
    import {onMount} from "svelte";

    const preferedSize = 8;
    let cursorScale = $state(1);
    let oldX = $state(0);
    let oldY = $state(0);
    let cursorX = $state(0);
    let cursorY = $state(0);
    let cursorWidth = $state(preferedSize);
    let cursorHeight = $state(preferedSize);
    let cursorDirection = $state(0);
    let visible = $state(false);

    onMount(() => {
        // Check for mobile (or touch screen computer)
        const touchDevice = ("ontouchstart" in window.document.documentElement)

        if (!touchDevice) {
            visible = true;
            let mouseMoveTimer : number;

            window.addEventListener('mousemove', (e) => {
                oldX = cursorX;
                oldY = cursorY;
                cursorX = e.clientX;
                cursorY = e.clientY;

                const cursorDistanceTraveled = Math.sqrt(Math.pow(cursorX - oldX, 2) + Math.pow(cursorY - oldY, 2));

                cursorWidth = preferedSize + (cursorDistanceTraveled / cursorScale);
                cursorDirection = Math.atan((cursorY - oldY) / (cursorX - oldX));

                clearTimeout(mouseMoveTimer);
                mouseMoveTimer = setTimeout(() => {
                    cursorWidth = preferedSize;
                }, 100);
            })

            window.document.body.addEventListener('mouseleave', () => {
                visible = false;
            })

            window.document.body.addEventListener('mouseenter', () => {
                visible = true;
            })
        }
    })
</script>

<span id="cursor"
      style="
      left: {(cursorX + oldX) / 2 - (cursorWidth / 2)}px;
      top: {(cursorY + oldY) / 2 - (cursorHeight / 2)}px;
      width: {cursorWidth}px;
      height: {cursorHeight}px;
      rotate: {cursorDirection}rad;
      scale: {cursorScale};
      display: {visible ? 'block' : 'none'};
"></span>

<style>
    #cursor {
        position: fixed;
        z-index: 1000;
        pointer-events: none;
        border-radius: 100%;
        background-color: white;
        mix-blend-mode: exclusion;
        filter: drop-shadow(0 0 2px #eee);
    }
</style>