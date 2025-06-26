<script lang="ts">
    let { name, pfp , attributes, pages, special = false } = $props();
</script>

<div class="container {special ? 'special' : ''}">
    <div class="title">
        <div class="imageContainer">
            <img src={pfp} alt={name}/>
            <div class="imageGlass"></div>
        </div>
        <div class="name">
            {#if special}&#x2605{/if}<b>{name}</b><br>
            {#each attributes as attr}
                <span class="personAttr">{attr}&nbsp; </span>
            {/each}
        </div>
    </div>
    <div class="links">
        {#each pages as page }
            <a href={page.link} target="_blank" tabindex="-1">
                <button class="dom">{page.type}</button>
            </a>
        {/each}
    </div>
</div>

<style lang="less">
    .container {
      padding: 4px;
      display: flex;
      flex-direction: column;
      gap: 4px;

      background: var(--dom-obj-bg-color);
      border: 1px solid var(--dom-obj-border-color);
      color: var(--primary-text-color);

      &.special {
        border: 1px solid var(--highlight-border-color);
        background: var(--highlight-bg-color);
      }
    }

    .title {
      display: flex;
      flex-direction: row;
      gap: 4px;
    }

    .name {
      padding: 8px;
      line-height: 1.5;
    }

    .links {
      display: flex;
      flex-direction: row;
      gap: 4px;
      justify-content: center;
    }

    .links a, button {
      width: 100%;
    }

    .imageContainer {
      width: 64px;
    }
</style>