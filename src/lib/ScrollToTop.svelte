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

<button onclick={top} style="position: {show ? 'sticky' : 'relative'}">
    &Uarr;
</button>

<style>
    button {
        transition: all 0.1s;
        margin-bottom: 4px;
        position: relative;
        bottom: 0;
        left: 0;
        background: var(--dom-obj-bg-color);
        border: 1px solid var(--dom-obj-border-color);
        color: var(--primary-text-color);
    }
    button:hover {
        border: 1px solid var(--primary-text-color);
    }
    button:active {
        background: var(--primary-text-color);
        color: var(--primary-text-color-inverted);
        border: 1px solid var(--primary-text-color);
    }
</style>
