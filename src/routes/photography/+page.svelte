<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import PhotoTile from "$lib/PhotoTile.svelte";
    import Title from "$lib/Title.svelte";
</script>

<main>
    <ToolBar />
    <div id="body">
        <Title text="&blk14;&blk12;&blk34;&block; April 5th Protest [HANDS OFF] &block;&blk34;&blk12;&blk14;"/>
        <div id="section">
            <PhotoTile photo="photos/april5thProtest/_MG_5456.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5458.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5483.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5500.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5545.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5548.jpg" alt="hi"/>
        </div>
        <Title text="&blk14;&blk12;&blk34;&block; Winter 2025 &block;&blk34;&blk12;&blk14;"/>
        <div id="section">
            <PhotoTile photo="photos/winter2025/_MG_5366.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5368.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5372.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5374.jpg" alt="hi"/>
        </div>
    </div>
</main>

<style>
    :root {
        font-family: 'Iosevka Web', monospace;
        line-height: 1.5;
        font-weight: 400;

        margin: 0;
        padding: 0;

        background-color: #242424;

        font-synthesis: none;
        text-rendering: optimizeLegibility;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    main {
        width: 650px;
    }
    #body {
        background: #191919;
        margin-top: 8px;
        margin-bottom: 8px;
    }
    #section {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
        grid-gap: 4px;
        margin-top: 4px;
        margin-bottom: 4px;
    }
</style>
