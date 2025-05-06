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
        background: var(--dom-obj-bg-color);
        border: 1px solid var(--dom-obj-border-color);
    }
    button:hover {
        border: 1px solid var(--primary-text-color);
    }
    button:active {
        background: var(--primary-text-color);
        border: 1px solid var(--primary-text-color);
        color: var(--primary-text-color-inverted);
    }
</style>
