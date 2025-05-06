<script lang="ts">
    import ToolBar from "$lib/ToolBar.svelte";
    import ScrollingTitle from "$lib/ScrollingTitle.svelte";
    import Footer from "$lib/Footer.svelte";
    import Wallpaper from "$lib/Wallpaper.svelte";
</script>

<main>
    <Wallpaper />
    <ScrollingTitle title="about "/>
    <ToolBar />
    <div id="body">
        <div id="profileHead">
            <div class="imageContainer">
                <img src="pfp.png" alt="profile"/>
                <div class="imageGlass">&Cross; PLACEHOLDER &Cross;<br/>Art by: @00_01d_ on twt.</div>
            </div>
            <div id="titleCard">
                <div id="abtme">
                    -> [&fnof;] about me
                </div>
                <div class="description">
                    &para; <b>Names</b>: Ave, burdne, urdons
                </div>
                <div class="description">
                    &#x2640; <b>Pronouns</b>: She/Her, They/Them
                </div>
                <div class="description">
                    &acd; <b>etc</b>: Transfem(&#x26A7;), Lesbian(&#x26A2;)
                </div>
            </div>
        </div>
        <div class="description">
            -> <b>Introduction</b>:<br/> Hello, I'm Ave. I'm a Computer Science student currently studying at Anne
            Arundel Community College and plan on transferring to a 4 year school. In my free time I work on small side
            <a href="/projects">projects</a> (like this website), draw, and take <a href="/photography">pictures</a>.
            I really enjoy graphic design, art, math (I know kinda random), music, and I'm ok at video games. My
            favorite show of all time is Neon Genesis Evangelion and my favorite character is Rei obv.!!!!
        </div>
        <div class="description">
            &bigodot; <b>Bands/Artists</b>:<br/>
            Beck, Radiohead/The Smile/Thom Yorke, C418, Tame Impala, Billie Eilish, Weezer, System of a Down,
            Arcade Fire, Car Seat Headrest, B&ocirc;a, Black Country New Road
        </div>
        <div class="description">
            &#x1FBC5; <b>Anime</b>:<br/>
            Neon Genesis Evangelion, Code Geass, Land of the Lustrous, Frieren, FLCL, Dungeon Meshi, Serial Experiments Lain
        </div>
        <div class="description">
            &curlyeqsucc; <b>Games</b>:<br/>
            Life is Strange, Portal, Half Life, BeamNG.drive, ENA Dream BBQ, Vintage Story, Minecraft, COD Black Ops 1
        </div>
        <div class="description">
            &ac; <b>People to check out</b>:<br/>
            <a href="https://atom596.com/">atom596.com</a>, <a href="https://hnasheralneam.dev/">hnasheralneam.dev</a>
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
        gap: 4px;
        margin-top: 4px;
        margin-bottom: 4px;
        background: var(--sub-bg-bg-color);
    }
    #profileHead {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4px;
    }
    #titleCard {
        display: flex;
        flex-direction: column;
        gap: 4px;
    }
    #abtme {
        line-height: 1.5;
        font-stretch: expanded;
        background: var(--sub-obj-bg-color);
        border: 1px solid var(--sub-obj-border-color);
        padding: 8px 12px;
        color: var(--secondary-text-color);
    }
    .description {
        line-height: 1.5;
        background: var(--dom-obj-bg-color);
        border: 1px solid var(--dom-obj-border-color);
        padding: 8px 12px;
    }
    b {
        font-weight: bolder;
    }
    .imageContainer {
        display: flex;
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
        color: black;
    }
</style>
