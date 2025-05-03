<script lang="ts">
    let { text } = $props();

    let open = $state(false);

    function handleClick() {
        open = !open;
    }
</script>

<button onclick={handleClick}>
    {open ? '⇈' : '⇊'}
    {text}
    {open ? '⇈' : '⇊'}
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
