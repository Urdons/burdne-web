<script lang="ts">
    import PhotoTile from "$lib/PhotoTile.svelte";
    import Dropdown from "$lib/Dropdown.svelte";

    let springOpen = $state(true);
    let protestOpen = $state(true);
    let winterOpen = $state(true);
</script>

<main>
    <div class="textBox sub">
        &boxbox; Photography
    </div>
    <section>
        <div class="textBox">
            <b>My Cameras</b>:<br>
            &Cross; Canon EOS Rebel t3 (2011)<br>
            &Cross; Asahi Pentax Spotmatic (1964)<br>
            &Cross; Minolta Maxxum 5 (2000)<br>
            &Cross; Polaroid Spirit 600 (1980s?)<br>
            &Cross; Polaroid Land 250 (1967)<br>
            <br>
            Directly below are links to other pages featuring more photos. <br>
            The <b>main</b> page contains digital photographs taken on my <b>Canon</b> DSLR camera. <br>
            The <b>film</b> page contains digital scans of film photographs taken my <b>Pentax</b> or <b>Minolta</b> SLR
            cameras.
        </div>
        <div class="linkContainer inset">
            <a href="/photography/film">
                <button class="dom">
                    Film Photographs ->
                </button>
            </a>
            <a href="/photography/AP2dArt">
                <button class="dom">
                    AP 2D Art Portfolio ->
                </button>
            </a>
        </div>
    </section>
    <Dropdown bind:open={springOpen} text="Spring 2025"/>
    <div style="display: {springOpen ? 'grid' : 'none'}" class="section">
        <PhotoTile photo="photos/spring2025/_MG_5424.jpg" alt="hi"/>
        <PhotoTile photo="photos/spring2025/_MG_5550.jpg" alt="hi"/>
        <PhotoTile photo="photos/spring2025/_MG_5551.jpg" alt="hi"/>
        <PhotoTile photo="photos/spring2025/_MG_5553.jpg" alt="hi"/>
    </div>
    <Dropdown bind:open={protestOpen} text="April 5th Protest [HANDS OFF]"/>
    <div style="display: {protestOpen ? 'grid' : 'none'}" class="section">
        <PhotoTile photo="photos/april5thProtest/_MG_5456.jpg" alt="hi"/>
        <PhotoTile photo="photos/april5thProtest/_MG_5458.jpg" alt="hi"/>
        <PhotoTile photo="photos/april5thProtest/_MG_5483.jpg" alt="hi"/>
        <PhotoTile photo="photos/april5thProtest/_MG_5500.jpg" alt="hi"/>
        <PhotoTile photo="photos/april5thProtest/_MG_5545.jpg" alt="hi"/>
        <PhotoTile photo="photos/april5thProtest/_MG_5548.jpg" alt="hi"/>
    </div>
    <Dropdown bind:open={winterOpen} text="Winter 2025"/>
    <div style="display: {winterOpen ? 'grid' : 'none'}" class="section">
        <PhotoTile photo="photos/winter2025/_MG_5366.jpg" alt="hi"/>
        <PhotoTile photo="photos/winter2025/_MG_5368.jpg" alt="hi"/>
        <PhotoTile photo="photos/winter2025/_MG_5372.jpg" alt="hi"/>
        <PhotoTile photo="photos/winter2025/_MG_5374.jpg" alt="hi"/>
    </div>
</main>

<style>
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
        justify-content: space-evenly;
    }
</style>
