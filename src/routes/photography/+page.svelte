<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import PhotoTile from "$lib/PhotoTile.svelte";
    import Title from "$lib/Title.svelte";
    import {onDestroy, onMount} from "svelte";

    let title = "photography ";
    let titleSpace = 12;
    let titleRoller : number;
    let rolledTitle = "burdne.com/loading...";
    let roll = 0;

    onMount(() => {
        titleRoller = setInterval(() => {
            rolledTitle = "burdne.com/"
            for (let i = 0; i < titleSpace; i++) {
                rolledTitle += title[(roll + i) % title.length];
            }
            roll++;
        }, 1000);
    });

    onDestroy(() => {
        clearInterval(titleRoller);
    });
</script>

<svelte:head>
    <title>{rolledTitle}</title>
</svelte:head>

<main>
    <ToolBar />
    <div id="body">
        <Title text="April 5th Protest [HANDS OFF]"/>
        <div id="section">
            <PhotoTile photo="photos/april5thProtest/_MG_5456.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5458.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5483.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5500.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5545.jpg" alt="hi"/>
            <PhotoTile photo="photos/april5thProtest/_MG_5548.jpg" alt="hi"/>
        </div>
        <Title text="Winter 2025"/>
        <div id="section">
            <PhotoTile photo="photos/winter2025/_MG_5366.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5368.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5372.jpg" alt="hi"/>
            <PhotoTile photo="photos/winter2025/_MG_5374.jpg" alt="hi"/>
        </div>
    </div>
</main>

<style>
    main {
        width: 650px;
    }
    #body {
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
