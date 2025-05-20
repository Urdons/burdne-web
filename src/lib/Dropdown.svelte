<script lang="ts">
    let { open = $bindable(false), text } = $props();

    function handleClick() {
        open = !open;
    }
</script>

<button class="dom {open ? 'open' : ''}" onclick={handleClick}>
    {open ? '⇊' : '⇈'}
    {text}
    {open ? '⇊' : '⇈'}
</button>

<style lang="less">
    button.open {
      background: var(--primary-text-color);
      border: 1px solid var(--primary-text-color);
      color: var(--primary-text-color-inverted);
      &:hover {
        background: var(--dom-obj-bg-color);
        color: var(--primary-text-color);
      }
      &:active {
        background: var(--dom-obj-bg-color);
        border: 1px solid var(--dom-obj-border-color);
        color: var(--primary-text-color);
      }
    }
</style>
