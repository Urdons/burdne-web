<script lang="ts">
    import { onMount } from 'svelte';

    let show = false;

    onMount(() => {
        window.addEventListener('scroll', () => {
            show = window.scrollY > 100;
        })
    })

    function top() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
    }
</script>

<button onclick={top} class="dom" style="bottom: {show ? '0' : '-64px'};">
    &Uarr;
</button>

<style>
    button {
        box-shadow: 0 0 8px var(--dom-bg-bg-color);
        transition: bottom 0.2s cubic-bezier(.29,0,0,1.41);
        z-index: 100;
        padding: 16px;
        margin: 8px;
        position: fixed;
        bottom: -64px;
        left: auto;
        mix-blend-mode: difference;
        filter: opacity(0.9);
    }
</style>
