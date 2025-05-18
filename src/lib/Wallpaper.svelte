<script lang="ts">
    import {onDestroy, onMount} from "svelte";

    let scroller : number;
    let offset = $state(0);

    onMount(() => {
        scroller = setInterval(() => {
            offset = offset + 2;
        }, 250);
    });

    onDestroy(() => {
        clearInterval(scroller);
    });
</script>

<div style="background-position: {offset}px {offset}px"></div>

<style>
    div {
        transition: background-position 1s linear;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        background-image: url("../wallpaper.png");
        background-repeat: repeat;
        image-rendering: pixelated;
        background-size: 128px;
        filter: opacity(10%);
    }
    @media (prefers-color-scheme: light) {
        div {
            filter: opacity(3%);
        }
    }
</style>
