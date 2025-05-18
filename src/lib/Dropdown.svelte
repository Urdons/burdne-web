<script lang="ts">
    let { open = $bindable(false), text } = $props();

    function handleClick() {
        open = !open;
    }
</script>

<button class="dom" onclick={handleClick}>
    {open ? '⇊' : '⇈'}
    {text}
    {open ? '⇊' : '⇈'}
</button>
