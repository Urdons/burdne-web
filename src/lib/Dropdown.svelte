<script lang="ts">
    let { open = $bindable(false), text } = $props();

    function handleClick() {
        open = !open;
    }
</script>

<button onclick={handleClick}>
    {open ? '⇊' : '⇈'}
    {text}
    {open ? '⇊' : '⇈'}
</button>

<style>
    button {
        background: #333;
        border: 1px solid #666;
    }
    button:hover {
        border: 1px solid white;
    }
    button:active {
        background: white;
        border: 1px solid white;
        color: black;
    }
</style>
