<script lang="ts">
    let { cover, title, artist, color = "transparent", subColor = color, stickerColor = "gray" } = $props();
</script>

<div class="album">
    <a href={cover} target="_blank" class="imageContainer">
        <img src={cover} alt={title}>
        <div class="imageGlass">&bigodot; {title}<br><br>&nbsp;♪ {artist}</div>
    </a>
    {#if color !== "transparent" }
        <div class="record" style='--color:{color}; --subColor:{subColor};'>
            <div class="recordSticker" style="--color:{stickerColor};"></div>
        </div>
    {/if}
</div>


<style>
    .imageContainer {
        z-index: 1;
        display: block;
    }
    .album {
        z-index: 0;
        display: block;
        &:hover {
            .record {
                transition: right 0.4s var(--bounce-function);
                right: -25%;
            }
            img, .imageGlass {
                transition: all 0.4s var(--bounce-function);
                transform: translateX(-25%);
            }
        }
    }
    img, .imageGlass {
        transition: all 0.4s cubic-bezier(0,1,.5,1);
    }
    .imageGlass {
        color: transparent;
        cursor: none;/*pointer*/
    }
    .record {
        transition: right 0.4s cubic-bezier(0,1,.5,1);
        z-index: 0;
        background: linear-gradient(to top, var(--color), var(--subColor));
        position: absolute;
        width: calc(100% - 4px);
        aspect-ratio: 1/1;
        border-radius: 100%;
        top: 2px;
        right: 2px;
        pointer-events: none;
        backdrop-filter: blur(2px);
    }
    .recordSticker {
        background: var(--color);
        border-radius: 100%;
        position: absolute;
        width: 30%;
        aspect-ratio: 1/1;
        top: 35%;
        left: 35%;
    }
</style>
