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

<button onclick={top} class="dom" style="position: {show ? 'sticky' : 'relative'}">
    &Uarr;
</button>

<style>
    button {
        margin-bottom: 4px;
        position: relative;
        bottom: 0;
        left: 0;
    }
</style>
