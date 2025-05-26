<script lang="ts">
    import Dropdown from "$lib/Dropdown.svelte";
    //import PhotoTile from "$lib/PhotoTile.svelte";

    let works = $state(true);
    let sheets = $state(false);
</script>

<main>
    <div class="textBox sub">
        &boxbox; AP 2D Art Portfolio (2023-2024)
    </div>
    <section>
        <div class="textBox">
            <b>THIS PAGE IS A WORK IN PROGESS</b>
        </div>
        <div class="linkContainer inset">
            <a href="/photography">
                <button class="dom">
                    &larr; Back to main page
                </button>
            </a>
        </div>
    </section>
    <Dropdown bind:open={works} text="Works" />
    <div style="display: {works ? 'grid' : 'none'}" class="section">

    </div>
    <Dropdown bind:open={sheets} text="Concept Sheets and Behind-the-Scenes" />
    <div style="display: {sheets ? 'grid' : 'none'}" class="section">

    </div>
</main>

<style lang="less">
  section {
    display: flex;
    flex-direction: column;
    background: var(--dom-obj-bg-color);
    border: 1px solid var(--dom-obj-border-color);
    color: var(--primary-text-color);
    gap: 4px;
    padding: 4px;
  }
  .section {
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    grid-gap: 4px;
  }
  .linkContainer {
    padding: 4px;
    display: flex;
  }
</style>
