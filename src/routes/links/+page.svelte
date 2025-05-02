<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import {onDestroy, onMount} from "svelte";

    let title = "links ";
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
        }, 500);
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
        <button>
            &block;&blk34;&blk12;&blk14;
        </button>
        <button>
            &blk14;&blk14;&blk14; LINKS PAGE UNDER CONSTRUCTION &blk14;&blk14;&blk14;
        </button>
    </div>
</main>

<style>
    main {
        width: 650px;
    }
    #body {
        margin-top: 4px;
        margin-bottom: 4px;
        background: #191919;
    }
</style>
