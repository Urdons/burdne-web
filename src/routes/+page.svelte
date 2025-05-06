<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import ScrollingTitle from "$lib/ScrollingTitle.svelte";
    import Footer from "$lib/Footer.svelte";
    import Wallpaper from "$lib/Wallpaper.svelte";
</script>

<main>
    <Wallpaper />
    <ScrollingTitle title="home "/>
    <ToolBar />
    <div id="body">
        <button>
            &block;&blk34;&blk12;&blk14;
        </button>
        <button>
            &blk14;&blk14;&blk14; HOME PAGE UNDER CONSTRUCTION &blk14;&blk14;&blk14;
        </button>
    </div>
    <Footer/>
</main>

<style>
    main {
        width: 650px;
    }
    #body {
        margin-top: 4px;
        margin-bottom: 4px;
        background: var(--sub-bg-bg-color);
    }
</style>
