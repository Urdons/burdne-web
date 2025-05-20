<script lang="ts">
    let { cover, title, artist } = $props();
</script>

<a href={cover} target="_blank" class="imageContainer">
    <img src={cover} alt={title}>
    <div class="imageGlass">&bigodot; {title}<br><br>&nbsp;♪ {artist}</div>
</a>

<style>
    .imageContainer {
        z-index: 1;
    }

    a {
        display: block;
    }
    .imageGlass {
        color: transparent;
        cursor: pointer;
    }
    .imageGlass:hover {
        color: var(--primary-text-color);
        text-shadow: 0 0 4px var(--primary-text-color-inverted);
    }
</style>
