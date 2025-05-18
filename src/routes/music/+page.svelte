<script lang="ts">
    import Album from "$lib/Album.svelte";
</script>

<main>
    <div class="textBox sub"> Good & Great Albums (by artist)</div>
    <div class="section">
        <Album coverImg="https://f4.bcbits.com/img/a2991836176_10.jpg"
               title="Forever Howlong"
               bandcamp="https://blackcountrynewroad.bandcamp.com/album/forever-howlong"
               appleMusic="https://music.apple.com/us/album/forever-howlong/1783713554"
               spotify="https://open.spotify.com/album/5FjaEW3Hi8vD2aoJNWln4t?si=W-qNgW9_T86fW-ZTC8ze0Q"
        />
        <Album coverImg="https://f4.bcbits.com/img/a4212377151_10.jpg"
               title="A Moon Shaped Pool"
               bandcamp="https://radiohead.bandcamp.com/album/a-moon-shaped-pool"
               appleMusic="https://music.apple.com/us/album/a-moon-shaped-pool/1111577743"
               spotify="https://open.spotify.com/album/2ix8vWvvSp2Yo7rKMiWpkg?si=jiZGHK7SQyKEJU_BVGdM6Q"
               special={true}
        />
        <Album coverImg="https://f4.bcbits.com/img/a1933083795_10.jpg"
               title="Wall Of Eyes"
               bandcamp="https://thesmile.bandcamp.com/album/wall-of-eyes"
               appleMusic="https://music.apple.com/us/album/wall-of-eyes/1711359135"
               spotify="https://open.spotify.com/album/6PdPOv5ybKZ9ZuGMk5iGZd?si=P56uI7d8QJiA2gAq05jguw"
        />
        <Album coverImg="https://upload.wikimedia.org/wikipedia/en/6/64/SystemofaDownToxicityalbumcover.jpg"
               title="Toxicity"
               appleMusic="https://music.apple.com/us/album/toxicity/273714443"
               spotify="https://open.spotify.com/album/6jWde94ln40epKIQCd8XUh?si=e8_ErlKxT7WcUtxmrsC8qw"
        />
        <Album coverImg="https://upload.wikimedia.org/wikipedia/en/9/9b/Tame_Impala_-_Currents.png"
               title="Currents"
               appleMusic="https://music.apple.com/us/album/currents/1440838039"
               spotify="https://open.spotify.com/album/79dL7FLiJFOO0EoehUHQBv?si=Z3lvztmHTqekddb176o1kQ"
               special={true}
        />
    </div>
    <section class="textBox sub">
        key:<br>
        &#x25B0; -> bandcamp<br>
        &#x266B;&nbsp; -> Apple Music<br>
        &cir; -> Spotify (no good alternative symbol)
    </section>
    <section class="textBox">
        All album art comes from the artist's official <a href="https://bandcamp.com/">&#x25B0;bandcamp</a> page.
        If the artist does not have a <a href="https://bandcamp.com/">&#x25B0;bandcamp</a> page, the art was
        found on the album's respective <a href="https://en.wikipedia.org/wiki/Main_Page">Wikipedia</a> page. I do
        not personally host the images, they are linked from the pages mentioned.
    </section>
</main>

<style>
    .section {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(128px, 1fr));
        gap: 4px;
    }
</style>
