<script lang="ts">
    let { photo, alt, link } = $props();

    let linklist : string[] = link.split('/');

    // remove the blank and src from the beginning
    linklist.reverse();
    linklist.pop();
    linklist.pop();
    linklist.reverse();

    link = "/src/" + linklist.join('/');
</script>

<div class="imageContainer">
    <a href={link}><!-- svelte-ignore --><enhanced:img src={photo} alt={alt}/></a>
    <div class="imageGlass">
        <button tabindex="-1">
            &bigotimes; &blk34;&blk12;&blk14; open your eyes &blk14;&blk12;&blk34; &bigotimes;
        </button>
    </div>
</div>

<style>
    enhanced\:img {
        transition: filter 2s ease-in-out;
        object-fit: cover;
        cursor: none;/*pointer*/
        filter: grayscale(100%) blur(2px) opacity(50%);
    }
    enhanced\:img:hover {
        transition: filter 0.2s ease-in-out;
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
