<script lang="ts">
    let { children } = $props();
    import { page } from "$app/state";
    import '../Iosevka.css';
    import '../reset.css';
    import '../app.less';
    import ToolBar from "$lib/ToolBar.svelte";
    import Wallpaper from "$lib/Wallpaper.svelte";
    import Footer from "$lib/Footer.svelte";
    import ScrollToTop from "$lib/ScrollToTop.svelte";
    import Cursor from "$lib/Cursor.svelte";

    const name = "burdne";
</script>

<svelte:head>
    <title>{name + page.url.pathname.split('/').join(" → ")}</title>
</svelte:head>

<main>
    <Wallpaper />
    <ToolBar />
    {@render children?.()}
    <Footer />
    <ScrollToTop />
    <Cursor />
</main>

<style lang="less">
  main {
    background: transparent;
    display: block;
    margin: 0;
    width: 650px;
    min-height: 100vh;
  }
</style>
