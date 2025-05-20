<script lang="ts">
    import PhotoTile from "$lib/PhotoTile.svelte";
    import Dropdown from "$lib/Dropdown.svelte";

    let springOpen = $state(true);
    let protestOpen = $state(true);
    let winterOpen = $state(true);
</script>

<main>
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
    .section {
        grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
        grid-gap: 4px;
    }
</style>
