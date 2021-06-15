<svelte:options tag="request-url" />

<script>
    export let url = "https://api.imgur.com/oauth2/token"
</script>

<style>
    .container {
        margin: 5px 12px 15px;
        padding: 6px 10px;
        background-color: rgb(248, 248, 248);
        border: 1px solid #ccc;
        font-size: 12px;
    }
</style>

<div class="container">{url}</div>