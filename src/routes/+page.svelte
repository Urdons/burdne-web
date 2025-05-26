<script lang="ts">
    import PersonProfile from "$lib/PersonProfile.svelte";
</script>

<main>
    <div class="textBox sub">
        &squ; home, things i like
    </div>
    <section class="landingZone">
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
        <div class="inset">
            <a href="/about">
                <button class="dom">
                    about me ->
                </button>
            </a>
            <a href="/links">
                <button class="dom">
                    links ->
                </button>
            </a>
            <a href="/photography">
                <button class="dom">
                    photography ->
                </button>
            </a>
            <a href="/rants">
                <button class="dom">
                    rants ->
                </button>
            </a>
            <p>
                <button class="dom">
                    button to click
                </button>
            </p>
        </div>
    </section>
    <div class="textBox sub">
        -> People I Like:
    </div>
    <div class="section">
        <PersonProfile name="autumn"
                       pfp="otherppl/autumn.png"
                       attributes={['friendo']}
                       pages={[
                           {type: 'web', link: 'https://atom596.com/'},
                           {type: 'bsky', link: 'https://bsky.app/profile/atom596.com'},
                           {type: 'git', link: 'https://github.com/EmpressAutumn'},
                           {type: 'yt', link: 'https://www.youtube.com/@aAtom596'},
                       ]}
                       special={true}
        />
        <PersonProfile name="blackshibe"
                       pfp="otherppl/blackshibe.jpg"
                       attributes={['programmer']}
                       pages={[
                           {type: 'web', link: 'https://blackshibe.net/'},
                           {type: 'git', link: 'https://github.com/blackshibe/'},
                           {type: 'sndcld', link: 'https://soundcloud.com/shibesongs'},
                       ]}
        />
        <PersonProfile name="cope"
                       pfp="otherppl/cope.jpg"
                       attributes={['friendo,', 'artist']}
                       pages={[
                           {type: 'twt', link: 'https://x.com/cope_ic'},
                           {type: 'bsky', link: 'https://bsky.app/profile/copeic.bsky.social'},
                           {type: 'insta', link: 'https://www.instagram.com/cope.thedoublefang/'},
                           {type: 'tik', link: 'https://www.tiktok.com/@cope.thedoublefang?is_from_webapp=1&sender_device=pc'},
                       ]}
                       special={true}
        />
        <PersonProfile name="hamza"
                       pfp="otherppl/hamza.jpg"
                       attributes={['friendo,', 'artist']}
                       pages={[
                           {type: 'web', link: 'https://hnasheralneam.dev/index.html'},
                           {type: 'git', link: 'https://github.com/hnasheralneam'},
                           {type: 'linkd', link: 'https://www.linkedin.com/in/hnasheralneam'},
                       ]}
                       special={true}
        />
    </div>
</main>

<style lang="less">
  .landingZone {
    background: var(--dom-obj-bg-color);
    border: 1px solid var(--dom-obj-border-color);
    display: flex;
    flex-direction: column;
    gap: 4px;
    padding: 4px;
  }

  .inset {
    padding: 4px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    gap: 4px;
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
</style>
