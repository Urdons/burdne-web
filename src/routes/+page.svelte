<main>
    <div class="textBox sub">
        &squ; home, things i like
    </div>
    <div class="landingZone">
        <div class="textBox centered special">
            &blk14;&blk14; Landing Zone &blk14;&blk14;
        </div>
        <section class="textBox">
            <b>Welcome</b> to my website!<br><br>
            I'm <b>burdne</b>, otherwise known as <b>burden</b>, <b>BurdenMeWithUrdons</b>, or <b>Urdons</b>. <br>
            To learn more about me, you can visit my <a href="/about">about me</a> page by clicking the link here or
            below. <br><br>
            This is my <b>landing/home page.</b> Below you will find <b>links</b> to other pages and a list of other
            people to check out.
        </section>
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
            <a href="/">
                <button class="dom">
                    button to click
                </button>
            </a>
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
                <a href="https://atom596.com/" target="_blank">
                    <button class="dom"> web</button>
                </a>
                <a href="https://bsky.app/profile/atom596.com" target="_blank">
                    <button class="dom"> bsky</button>
                </a>
                <a href="https://github.com/EmpressAutumn" target="_blank">
                    <button class="dom"> git</button>
                </a>
                <a href="https://www.youtube.com/@aAtom596" target="_blank">
                    <button class="dom"> yt</button>
                </a>
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
                <a href="https://blackshibe.net/" target="_blank">
                    <button class="dom"> web</button>
                </a>
                <a href="https://github.com/blackshibe/" target="_blank">
                    <button class="dom"> git</button>
                </a>
                <a href="https://soundcloud.com/shibesongs" target="_blank">
                    <button class="dom"> sndcld</button>
                </a>
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
                <a href="https://x.com/cope_ic" target="_blank">
                    <button class="dom"> twt</button>
                </a>
                <a href="https://bsky.app/profile/copeic.bsky.social" target="_blank">
                    <button class="dom"> bsky</button>
                </a>
                <a href="https://www.instagram.com/cope.thedoublefang/" target="_blank">
                    <button class="dom"> insta</button>
                </a>
                <a href="https://www.tiktok.com/@cope.thedoublefang?is_from_webapp=1&sender_device=pc" target="_blank">
                    <button class="dom"> tik</button>
                </a>
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
                <a href="https://hnasheralneam.dev/index.html" target="_blank">
                    <button class="dom"> web</button>
                </a>
                <a href="https://github.com/hnasheralneam" target="_blank">
                    <button class="dom"> git</button>
                </a>
                <a href="https://www.linkedin.com/in/hnasheralneam" target="_blank">
                    <button class="dom"> linkd</button>
                </a>
            </div>
        </div>
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
    justify-content: center;
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

  .personProfile {
    padding: 4px;
    display: flex;
    flex-direction: column;
    gap: 4px;

    background: var(--dom-obj-bg-color);
    border: 1px solid var(--dom-obj-border-color);
    color: var(--primary-text-color);

    &.special {
      border: 1px solid var(--highlight-border-color);
      background: var(--highlight-bg-color);
    }
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

  .personLinks a, button {
    width: 100%;
  }

  .imageContainer {
    width: 64px;
  }
</style>
