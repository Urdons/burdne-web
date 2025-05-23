<script>
    let { coverImg, title, artist, discogs = "", bandcamp = "", appleMusic = "", spotify = "", special = false, recordColor = "transparent", recordOutline = recordColor, stickerColor = "gray" } = $props();

    import AlbumCover from "$lib/AlbumCover.svelte";
</script>

<div class="album">
    <AlbumCover cover={coverImg} title={title} artist={artist}/>
    {#if recordColor !== "transparent" }
        <div class="record" style='--color:{recordColor}; --outline:{recordOutline};'>
            <div class="recordSticker" style="--color:{stickerColor};"></div>
        </div>
    {/if}
    <div class="linkContainer">
        {#if discogs.length > 0}
            <a href={discogs} target="_blank">
                <button class={special ? "special" : ""}>
                    &bigodot;
                </button>
            </a>
        {:else }
            <p>
                <button disabled>
                    &bigodot;
                </button>
            </p>
        {/if}
        {#if bandcamp.length > 0}
            <a href={bandcamp} target="_blank">
                <button class={special ? "special" : ""}>
                    &#x25B0;
                </button>
            </a>
        {:else }
            <p>
                <button disabled>
                    &#x25B0;
                </button>
            </p>
        {/if}
        {#if appleMusic.length > 0}
            <a href={appleMusic} target="_blank">
                <button class={special ? "special" : ""}>
                    &#x266B;
                </button>
            </a>
        {:else }
            <p>
                <button disabled>
                    &#x266B;
                </button>
            </p>
        {/if}
        {#if spotify.length > 0}
            <a href={spotify}
               target="_blank">
                <button class={special ? "special" : ""}>
                    &cir;
                </button>
            </a>
        {:else }
            <p>
                <button disabled>
                    &#x266B;
                </button>
            </p>
        {/if}
    </div>
</div>

<style lang="less">
  div {
    border: none;
    position: relative;
  }

  .record {
    background: linear-gradient(to top, var(--color), var(--outline));
    border: 1px solid var(--outline);
    position: absolute;
    width: calc(100% - 4px);
    aspect-ratio: 1/1;
    border-radius: 100%;
    top: 1px;
    right: 1px;
    pointer-events: none;
    backdrop-filter: blur(4px);
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
  .album:hover {
    z-index: 10;
    .record {
      transition: right 0.2s var(--bounce-function);
      right: -50%;
    }
  }

  .linkContainer {
    transition: top 0.1s ease-in-out;
    display: flex;
    position: relative;
    flex-direction: row;
    justify-content: space-between;
  }

  .linkContainer a, p, button {
    width: 100%;
  }
  button {
    padding-left: 0;
    padding-right: 0;
  }
</style>
