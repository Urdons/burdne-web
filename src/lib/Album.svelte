<script>
    let { coverImg, title, bandcamp = "", appleMusic = "", spotify = "", special = false } = $props();

    import AlbumCover from "$lib/AlbumCover.svelte";
</script>

<div class={special ? "special" : ""}>
    <AlbumCover cover={coverImg} title={title}/>
    <div class="linkContainer">
        {#if bandcamp.length > 0}
            <a href={bandcamp} target="_blank">
                <button>
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
                <button>
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
                <button>
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
  }

  .linkContainer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .linkContainer a, p, button {
    width: 100%;
  }

  .special button {
    background: var(--highlight-bg-color);
    border: 1px solid var(--highlight-border-color);
    color: var(--primary-text-color);
    &:hover {
      border: 1px solid var(--primary-text-color);
    }
    &:active {
      background: var(--primary-text-color);
      border: 1px solid var(--primary-text-color);
      color: var(--primary-text-color-inverted);
    }
  }
</style>
