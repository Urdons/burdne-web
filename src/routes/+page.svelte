<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
</script>

<main>
    <ToolBar />
    <div id="body">
        <button>
            &block;&blk34;&blk12;&blk14;
        </button>
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
        margin-top: 8px;
        margin-bottom: 8px;
        background: #191919;
    }
</style>
