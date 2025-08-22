<script lang="ts">
    import Dropdown from "$lib/Dropdown.svelte";
    import PhotoTile from "$lib/PhotoTile.svelte";

    const worksImgs = import.meta.glob(
        '/src/photos/ap2dart/works/*.{avif,gif,heif,jpeg,jpg,png,tiff,webp,svg}',
        { eager: true, query: { enhanced: true } }
    )
    const sheetsImgs = import.meta.glob(
        '/src/photos/ap2dart/bts/*.{avif,gif,heif,jpeg,jpg,png,tiff,webp,svg}',
        { eager: true, query: { enhanced: true } }
    )

    let works = $state(true);
    let sheets = $state(false);
</script>

<main>
    <div class="textBox sub">
        &boxbox; AP 2D Art Portfolio (2023-2024)
    </div>
    <section>
        <div class="textBox">
            <b>Inquiry:</b><br>
            I have a strong interest in what mechanical mysteries go on behind the scenes. I take apart and
            build computers, program websites and applications, and fix things myself when they break. With my
            inquiry I decided build off of this interest by photographing and presenting the mechanics behind everyday
            items and tools while creating unique compositions.
        </div>
        <div class="linkContainer inset">
            <a href="/photography" tabindex="-1">
                <button class="dom">
                    &larr; Back to main page
                </button>
            </a>
        </div>
    </section>
    <Dropdown bind:open={works} text="Works" />
    <div style="display: {works ? 'grid' : 'none'}" class="section">
        {#each Object.entries(worksImgs) as [_path, module]}
            <PhotoTile photo={module.default} link={_path} alt="hi"/>
        {/each}
    </div>
    <Dropdown bind:open={sheets} text="Concept Sheets and Behind-the-Scenes" />
    <div style="display: {sheets ? 'grid' : 'none'}" class="section">
        {#each Object.entries(sheetsImgs) as [_path, module]}
            <PhotoTile photo={module.default} link={_path} alt="hi"/>
        {/each}
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
