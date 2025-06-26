<script lang="ts">
    import Dropdown from "$lib/Dropdown.svelte";
    import PhotoTile from "$lib/PhotoTile.svelte";

    let fall2024 = $state(true);
</script>

<main>
    <div class="textBox sub">
        &boxbox; Film Photography
    </div>
    <section>
        <div class="textBox">
            <b>Featured Film Cameras</b>:<br>
            &Cross; Asahi Pentax Spotmatic (1964)<br>
            &Cross; Minolta Maxxum 5 (2000)<br>
            <br>
            <b>Favorite 35mm Film</b>:<br>
            &Cross; Ilford HP5 (or really any of their B&W film)<br>
            &Cross; Harman Phoenix<br>
            &Cross; Kodak Colorplus 200 (I know, controversial)<br>
            &Cross; Fujicolor 200<br>
            <br>
            To return to the main page, click the link below
        </div>
        <div class="linkContainer inset">
            <a href="/photography" tabindex="-1">
                <button class="dom">
                    &larr; Back to main page
                </button>
            </a>
        </div>
    </section>
    <Dropdown bind:open={fall2024} text="Fall 2024" />
    <div style="display: {fall2024 ? 'grid' : 'none'}" class="section">
        <PhotoTile photo="/photos/film/fall2024/000773260017.jpg" alt="hi"/>
        <PhotoTile photo="/photos/film/fall2024/000773260018.jpg" alt="hi"/>
        <PhotoTile photo="/photos/film/fall2024/000773260020.jpg" alt="hi"/>
        <PhotoTile photo="/photos/film/fall2024/000773260025.jpg" alt="hi"/>
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
