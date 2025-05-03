<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import PhotoTile from "$lib/PhotoTile.svelte";
    import Dropdown from "$lib/Dropdown.svelte";
    import ScrollingTitle from "$lib/ScrollingTitle.svelte";
    import Footer from "$lib/Footer.svelte";
</script>

<main>
    <ScrollingTitle title="photography "/>
    <ToolBar />
    <div id="body">
        <Dropdown text="April 5th Protest [HANDS OFF]"/>
        <div id="section">
            <PhotoTile photo="photos/april5thProtest/_MG_5456.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5458.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5483.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5500.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5545.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5548.jpg" alt="hi"/>
        </div>
        <Dropdown text="Winter 2025"/>
        <div id="section">
            <PhotoTile photo="photos/winter2025/_MG_5366.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5368.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5372.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5374.jpg" alt="hi"/>
        </div>
    </div>
    <Footer />
</main>

<style>
    main {
        width: 650px;
    }
    #body {
        display: flex;
        flex-direction: column;
        background: #191919;
        margin-top: 4px;
        margin-bottom: 4px;
    }
    #section {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
        grid-gap: 4px;
        margin-top: 4px;
        margin-bottom: 4px;
    }
</style>
