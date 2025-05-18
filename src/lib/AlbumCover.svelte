<script lang="ts">
    let { cover, title } = $props();
</script>

<div class="imageContainer">
    <img src={cover} alt={title}>
    <div class="imageGlass">{title}</div>
</div>

<style>
    .imageGlass {
        color: transparent;
    }
    .imageGlass:hover {
        color: var(--primary-text-color);
    }
</style>
