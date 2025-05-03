<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import ScrollingTitle from "$lib/ScrollingTitle.svelte";
    import Footer from "$lib/Footer.svelte";
</script>

<main>
    <ScrollingTitle title="links "/>
    <ToolBar />
    <div id="body">
        <a href="https://www.youtube.com/@urdons"><button>
            &RightTriangle; youtube
        </button></a>
        <a href="https://www.instagram.com/ave_wiernicki/"><button>
            &square; instagram
        </button></a>
        <a href="https://x.com/Urdons"><button>
            &Cross; twitter
        </button></a>
        <a href="https://bsky.app/profile/burdne.bsky.social"><button>
            &apid; bluesky
        </button></a>
        <a href="https://github.com/Urdons"><button>
            &uarr; github
        </button></a>
    </div>
    <Footer/>
</main>

<style>
    main {
        width: 650px;
    }
    #body {
        display: flex;
        flex-direction: column;
        gap: 4px;
        margin-top: 4px;
        margin-bottom: 4px;
        background: #191919;
    }
    a {
        width: 100%;
    }
    button {
        background: #333;
        width: 100%;
        border: 1px solid #666;
        color: white;
    }
    button:hover {
        border: 1px solid white;
    }
    button:active {
        background: white;
        color: black;
        border: 1px solid white;
    }
</style>
