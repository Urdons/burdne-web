<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";

    import Footer from "$lib/Footer.svelte";
    import Wallpaper from "$lib/Wallpaper.svelte";
    import ScrollToTop from "$lib/ScrollToTop.svelte";
</script>

<main>
    <Wallpaper />
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
        <a href="https://steamcommunity.com/id/Urdons/"><button>
            &#x2622; steam
        </button></a>
        <a href="https://github.com/Urdons"><button>
            &rarrlp; github
        </button></a>
    </div>
    <Footer/>
    <ScrollToTop/>
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
        background: var(--sub-bg-bg-color);
    }
    a {
        width: 100%;
    }
    button {
        background: var(--dom-obj-bg-color);
        width: 100%;
        border: 1px solid var(--dom-obj-border-color);
        color: var(--primary-text-color);
    }
    button:hover {
        border: 1px solid var(--primary-text-color);
    }
    button:active {
        background: var(--primary-text-color);
        color: var(--primary-text-color-inverted);
        border: 1px solid var(--primary-text-color);
    }
</style>
