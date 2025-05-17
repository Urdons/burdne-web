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
        <div class="textBox sub">
            &squ; home, things i like
        </div>
        <div class="landingZone">
            <div class="textBox centered special">
                &blk14;&blk14; Landing Zone &blk14;&blk14;
            </div>
            <div class="textBox">
                <b>Welcome</b> to my website!<br><br>
                I'm <b>burdne</b>, otherwise known as <b>burden</b>, <b>BurdenMeWithUrdons</b>, or <b>Urdons</b>. <br>
                To learn more about me, you can visit my <a href="/about">about me</a> page by clicking the link here or
                below. <br><br>
                This is my <b>landing/home page.</b> Below you will find <b>links</b> to other pages and a list of other
                people to check out.
            </div>
            <div class="landingLinkContainer">
                <a href="/about"><button>
                    about me ->
                </button></a>
                <a href="/links"><button>
                    links ->
                </button></a>
                <a href="/photography"><button>
                    photography ->
                </button></a>
                <a href="/rants"><button>
                    rants ->
                </button></a>
                <a href="/"><button>
                    button to click
                </button></a>
            </div>
        </div>
        <div class="textBox sub">
            -> People I Like:
        </div>
        <div class="section">
            <div class="personProfile special">
                <div class="personTitle">
                    <div class="imageContainer">
                        <img src="otherppl/autumn.png" alt="autumn"/>
                        <div class="imageGlass"></div>
                    </div>
                    <div class="personName">
                        &#x2605<b>autumn</b><br>
                        friendo
                    </div>
                </div>
                <div class="personLinks">
                    <a href="https://atom596.com/" target="_blank"><button> web </button></a>
                    <a href="https://bsky.app/profile/atom596.com" target="_blank"><button> bsky </button></a>
                    <a href="https://github.com/EmpressAutumn" target="_blank"><button> git </button></a>
                    <a href="https://www.youtube.com/@aAtom596" target="_blank"><button> yt </button></a>
                </div>
            </div>
            <div class="personProfile">
                <div class="personTitle">
                    <div class="imageContainer">
                        <img src="otherppl/blackshibe.jpg" alt="blackshibe"/>
                        <div class="imageGlass"></div>
                    </div>
                    <div class="personName">
                        <b>blackshibe</b><br>
                        developer, artist
                    </div>
                </div>
                <div class="personLinks">
                    <a href="https://blackshibe.net/" target="_blank"><button> web </button></a>
                    <a href="https://github.com/blackshibe/" target="_blank"><button> git </button></a>
                    <a href="https://soundcloud.com/shibesongs" target="_blank"><button> sndcld </button></a>
                </div>
            </div>
            <div class="personProfile special">
                <div class="personTitle">
                    <div class="imageContainer">
                        <img src="otherppl/cope.jpg" alt="cope_ic"/>
                        <div class="imageGlass"></div>
                    </div>
                    <div class="personName">
                        &#x2605<b>cope_ic</b><br>
                        friendo, artist
                    </div>
                </div>
                <div class="personLinks">
                    <a href="https://x.com/cope_ic" target="_blank"><button> twt </button></a>
                    <a href="https://bsky.app/profile/copeic.bsky.social" target="_blank"><button> bsky </button></a>
                    <a href="https://www.instagram.com/cope.thedoublefang/" target="_blank"><button> insta </button></a>
                    <a href="https://www.tiktok.com/@cope.thedoublefang?is_from_webapp=1&sender_device=pc" target="_blank"><button> tik </button></a>
                </div>
            </div>
            <div class="personProfile special">
                <div class="personTitle">
                    <div class="imageContainer">
                        <img src="otherppl/hamza.jpg" alt="hamza"/>
                        <div class="imageGlass"></div>
                    </div>
                    <div class="personName">
                        &#x2605<b>hamza</b><br>
                        friendo, programmer
                    </div>
                </div>
                <div class="personLinks">
                    <a href="https://hnasheralneam.dev/index.html" target="_blank"><button> web </button></a>
                    <a href="https://github.com/hnasheralneam" target="_blank"><button> git </button></a>
                    <a href="https://www.linkedin.com/in/hnasheralneam" target="_blank"><button> linkd </button></a>
                </div>
            </div>
        </div>
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
    .landingZone {
        background: var(--dom-obj-bg-color);
        border: 1px solid var(--dom-obj-border-color);
        display: flex;
        flex-direction: column;
        gap: 4px;
        padding: 4px;
    }
    .landingLinkContainer {
        padding: 4px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 4px;
        background-color: var(--sub-bg-bg-color);
        border: 1px solid var(--sub-obj-border-color);
    }
    .textBox.centered {
        text-align: center;
    }
    b {
        font-weight: bolder;
    }
    .section {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
        grid-gap: 4px;
    }
    .personProfile {
        padding: 4px;
        background: var(--dom-obj-bg-color);
        border: 1px solid var(--dom-obj-border-color);
        display: flex;
        flex-direction: column;
        gap: 4px;
    }
    .special {
        border: 1px solid var(--highlight-border-color);
        background: var(--highlight-bg-color);
    }
    .personTitle {
        display: flex;
        flex-direction: row;
        gap: 4px;
    }
    .personName {
        padding: 8px;
        line-height: 1.5;
    }
    .personLinks {
        display: flex;
        flex-direction: row;
        gap: 4px;
        justify-content: center;
    }
    .personLinks a {
        width: 100%;
    }
    .personLinks button {
        width: 100%;
        height: 100%;
    }
    .imageContainer {
        width: 64px;
        overflow: hidden;
        aspect-ratio: 1/1;
        position: relative;
    }
    img {
        object-fit: cover;
        width: 100%;
        height: 100%;
    }
    .imageGlass {
        position: absolute;
        top: 1px;
        left: 1px;
        width: calc(100% - 2px);
        height: calc(100% - 2px);
        outline: 1px solid var(--glass-border);
    }
</style>
