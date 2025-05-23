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
        transition: bottom 0.2s var(--bounce-function);
        z-index: 100;
        padding: 16px;
        margin: 8px;
        position: fixed;
        bottom: -64px;
        left: auto;
        background: #77777744;
        border: solid 1px #77777744;
        color: white;
        backdrop-filter: blur(4px);
    }
</style>
