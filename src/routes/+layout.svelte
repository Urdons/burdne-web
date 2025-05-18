<script>
    import { page } from "$app/state";
    import '../reset.css';
    import '../app.less';
    import ToolBar from "$lib/ToolBar.svelte";
    import Wallpaper from "$lib/Wallpaper.svelte";
    import Footer from "$lib/Footer.svelte";
    import ScrollToTop from "$lib/ScrollToTop.svelte";

    const name = "burdne";
    console.log(page.url.pathname);
</script>

<svelte:head>
    <title>{name + page.url.pathname.split('/').join(" → ")}</title>
</svelte:head>

<main>
    <Wallpaper />
    <ToolBar />
    <slot />
    <Footer/>
    <ScrollToTop/>
</main>

<style lang="less">
  main {
    background: transparent;
    display: block;
    margin: 0;
    width: 650px;
  }
</style>
