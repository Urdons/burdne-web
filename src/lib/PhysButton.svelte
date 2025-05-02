<script lang="ts">
    let { text = "unnamed", onClick = function () {console.log("button")} } = $props();
</script>

<button onclick={onClick} class="physButtonBack">
    <div class="physButtonFront">
        {text}
    </div>
</button>

<style>
    .physButtonBack {
        position: relative;
        background: #00000044;
        border: solid 2px #00000000;
        border-radius: 4px;
        padding: 0;
        margin: 0;
    }

    .physButtonFront {
        position: relative;
        top: -2px;
        background: #666;
        border-bottom: solid 2px #444;
        border-radius: 4px;
        color: white;
        font-family: 'Iosevka Web', monospace;
        font-stretch: expanded;
        padding: 8px 12px;
    }
    .physButtonFront:hover {
        background: #707070;
        top: -3px;
    }
    .physButtonFront:active {
        background: #555;
        top: 0;
    }
</style>