<script lang="ts">
    let { text } = $props();
</script>

<div>
    <p>||||</p>
    <p class="title">{text}</p>
    <p>||||</p>
</div>

<style>
    div {
        display: flex;
        justify-content: space-between;
        background: #242424;
        color: #555;
        border: 1px solid #555;
        padding: 8px 4px;
        font-family: 'Iosevka Web', monospace;
        font-stretch: expanded;
        text-overflow: ellipsis;
    }
    p {
        pointer-events: none;
    }
    .title {
        color: white;
    }
</style>
