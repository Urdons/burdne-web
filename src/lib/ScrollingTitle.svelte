<script lang="ts">
    let { title } = $props();
    //import {onDestroy, onMount} from "svelte";

    //let titleSpace = 12;
    //let titleRoller : number;
    let rolledTitle = $state("burdne → " + title);
    //let roll = 0;

    /*
    onMount(() => {
        titleRoller = setInterval(() => {
            rolledTitle = "burdne.com/"
            for (let i = 0; i < titleSpace; i++) {
                rolledTitle += title[(roll + i) % title.length];
            }
            roll++;
        }, 500);
    });

    onDestroy(() => {
        clearInterval(titleRoller);
    });
     */
</script>

<svelte:head>
    <title>{rolledTitle}</title>
</svelte:head>
