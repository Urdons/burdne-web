<script lang="ts">
    let { cover, title } = $props();
</script>

<div class="photoTile">
    <img class="photoTileImg" src={cover} alt={title}>
    <div class="photoTileGlass">{title}</div>
</div>

<style>
    .photoTile {
        overflow: hidden;
        aspect-ratio: 1/1;
        position: relative;
        width: 100%;
        height: 100%;
    }
    .photoTileImg {
        object-fit: cover;
        cursor: default;
        width: 100%;
    }
    .photoTileGlass {
        top: 1px;
        left: 1px;
        width: calc(100% - 2px);
        height: calc(100% - 2px);
        display: flex;
        position: absolute;
        outline: 1px solid var(--glass-border);
        color: transparent;
    }
    .photoTileGlass:hover {
        color: var(--primary-text-color);
    }
</style>
