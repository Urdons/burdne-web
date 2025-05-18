<script lang="ts">
    let { photo, alt, link = photo } = $props();
</script>

<div class="imageContainer">
    <a href={link}><img src={photo} alt={alt}></a>
    <div class="imageGlass">
        <button>
            &bigotimes; &blk34;&blk12;&blk14; open your eyes &blk14;&blk12;&blk34; &bigotimes;
        </button>
    </div>
</div>

<style>
    img {
        transition: filter 0.2s ease-in-out;
        object-fit: cover;
        cursor: pointer;
        filter: grayscale(100%) blur(2px) opacity(50%);
    }
    img:hover {
        filter: grayscale(0%);
    }
    .imageGlass {
        display: flex;
        justify-content: center;
        align-items: center;
        pointer-events: none;
    }
    button {
        background: transparent;
        border: 1px dotted var(--primary-text-color);
    }
</style>
