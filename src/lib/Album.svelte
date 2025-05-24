<script>
    let { discogs = "", bandcamp = "", appleMusic = "", spotify = "", special = false, children } = $props();
</script>

<div class="album">
    {@render children()}
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
                    &cir;
                </button>
            </p>
        {/if}
    </div>
</div>

<style lang="less">
  .album:hover {
    z-index: 5;
  }
  div {
    border: none;
    position: relative;
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
