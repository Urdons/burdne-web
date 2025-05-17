<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import Footer from "$lib/Footer.svelte";
    import Wallpaper from "$lib/Wallpaper.svelte";
    import ScrollToTop from "$lib/ScrollToTop.svelte";
    import AlbumCover from "$lib/AlbumCover.svelte";
</script>

<main>
    <Wallpaper />
    <ToolBar />
    <div id="body">
        <div class="textBox sub"> Good & Great Albums (by artist) </div>
        <div class="section">
            <div class="albumContainer">
                <AlbumCover cover="music/ForeverHowlong.jpg" title="Forever Howlong"/>
                <div class="albumLinkContainer">
                    <a href="https://blackcountrynewroad.bandcamp.com/album/forever-howlong" target="_blank"><button>
                        &#x25B0;
                    </button></a>
                    <a href="https://music.apple.com/us/album/forever-howlong/1783713554" target="_blank"><button>
                        &#x266B;
                    </button></a>
                    <a href="https://open.spotify.com/album/5FjaEW3Hi8vD2aoJNWln4t?si=W-qNgW9_T86fW-ZTC8ze0Q" target="_blank"><button>
                        &cir;
                    </button></a>
                </div>
            </div>
            <div class="albumContainer special">
                <AlbumCover cover="music/AMoonShapedPool.jpg" title="A Moon Shaped Pool"/>
                <div class="albumLinkContainer">
                    <a href="https://radiohead.bandcamp.com/album/a-moon-shaped-pool" target="_blank"><button>
                        &#x25B0;
                    </button></a>
                    <a href="https://music.apple.com/us/album/a-moon-shaped-pool/1111577743" target="_blank"><button>
                        &#x266B;
                    </button></a>
                    <a href="https://open.spotify.com/album/2ix8vWvvSp2Yo7rKMiWpkg?si=jiZGHK7SQyKEJU_BVGdM6Q" target="_blank"><button>
                        &cir;
                    </button></a>
                </div>
            </div>
            <div class="albumContainer">
                <AlbumCover cover="music/WallOfEyes.jpg" title="Wall of Eyes"/>
                <div class="albumLinkContainer">
                    <a href="https://thesmile.bandcamp.com/album/wall-of-eyes" target="_blank"><button>
                        &#x25B0;
                    </button></a>
                    <a href="https://music.apple.com/us/album/wall-of-eyes/1711359135" target="_blank"><button>
                        &#x266B;
                    </button></a>
                    <a href="https://open.spotify.com/album/6PdPOv5ybKZ9ZuGMk5iGZd?si=P56uI7d8QJiA2gAq05jguw" target="_blank"><button>
                        &cir;
                    </button></a>
                </div>
            </div>
            <div class="albumContainer">
                <AlbumCover cover="music/Toxicity.jpg" title="Toxicity"/>
                <div class="albumLinkContainer">
                    <p><button class="disabled">
                        &#x25B0;
                    </button></p>
                    <a href="https://music.apple.com/us/album/toxicity/273714443" target="_blank"><button>
                        &#x266B;
                    </button></a>
                    <a href="https://open.spotify.com/album/6jWde94ln40epKIQCd8XUh?si=e8_ErlKxT7WcUtxmrsC8qw" target="_blank"><button>
                        &cir;
                    </button></a>
                </div>
            </div>
            <div class="albumContainer special">
                <AlbumCover cover="music/Currents.png" title="Currents"/>
                <div class="albumLinkContainer">
                    <p><button class="disabled">
                        &#x25B0;
                    </button></p>
                    <a href="https://music.apple.com/us/album/currents/1440838039" target="_blank"><button>
                        &#x266B;
                    </button></a>
                    <a href="https://open.spotify.com/album/79dL7FLiJFOO0EoehUHQBv?si=Z3lvztmHTqekddb176o1kQ" target="_blank"><button>
                        &cir;
                    </button></a>
                </div>
            </div>
        </div>
        <div class="textBox sub">
            key:<br>
            &#x25B0; -> bandcamp<br>
            &#x266B;&nbsp; -> Apple Music<br>
            &cir; -> Spotify (no good alternative symbol)
        </div>
        <div class="textBox">
            All album art comes from the artist's official <a href="https://bandcamp.com/">&#x25B0;bandcamp</a> page.
            If the artist does not have a <a href="https://bandcamp.com/">&#x25B0;bandcamp</a> page, the art was
            found on the album's respective <a href="https://en.wikipedia.org/wiki/Main_Page">Wikipedia</a> page.
        </div>
    </div>
    <Footer />
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
    .section {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(128px, 1fr));
        gap: 4px;
    }
    .albumContainer {
        display: flex;
        flex-direction: column;
    }
    .albumLinkContainer {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .albumLinkContainer a {
        width: 100%;
    }
    .albumLinkContainer p {
        width: 100%;
    }
    .albumLinkContainer button {
        width: 100%;
    }
    .special  button {
        background: var(--highlight-bg-color);
        border: 1px solid var(--highlight-border-color);
        color: var(--primary-text-color);
    }
    .special  button:hover {
        border: 1px solid var(--primary-text-color);
    }
    .special  button:active {
        background: var(--primary-text-color);
        border: 1px solid var(--primary-text-color);
        color: var(--primary-text-color-inverted);
    }
</style>
