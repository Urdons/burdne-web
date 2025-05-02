<script lang="ts">
    let { photo, alt } = $props();
</script>

<div class="photoTile">
    <img class="photoTileImg" src={photo} alt={alt}>
    <div class="photoTileGlass">
        <button>
            &bigotimes; &blk34;&blk12;&blk14; open your eyes &blk14;&blk12;&blk34; &bigotimes;
        </button>
    </div>
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
        transition: filter 0.2s ease-in-out;
        object-fit: cover;
        cursor: pointer;
        width: 100%;
        height: 100%;
        filter: grayscale(100%) blur(2px) brightness(0.5);
    }
    .photoTileImg:hover {
        filter: grayscale(0%);
    }
    .photoTileGlass {
        top: 1px;
        left: 1px;
        width: calc(100% - 2px);
        height: calc(100% - 2px);
        display: flex;
        position: absolute;
        justify-content: center;
        align-items: center;
        pointer-events: none;
        outline: 1px solid #ffffff44;
    }
    button {
        background: transparent;
        border: 1px solid white;
    }
</style>
