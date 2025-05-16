<script>
    import { page } from "$app/state";
    import '../reset.css';
    import '../app.css';

    const name = "burdne";
    console.log(page.url.pathname);
</script>

<svelte:head>
    <title>{name + page.url.pathname.split('/').join(" → ")}</title>
</svelte:head>

<slot />