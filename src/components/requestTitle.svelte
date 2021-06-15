<svelte:options tag="request-title" />

<script>
    export let method = "POST"
    export let title = "Generate Access Token"
    let red = "#ff0000"
</script>

<style>
    .container {
        padding: 12px;
    }
    .method {
        font-size: 16px;
        font-weight: bold;
    }
    .method.post {
        color: rgb(255, 180, 0);
    }
    .method.get {
        color: rgb(12, 187, 82);
    }
    .title {
        color: rgb(40, 40, 40);
        font-size: 16px;
        font-weight: bold;
    }
</style>

<div class="container">
    <span class={`method ${method.toLowerCase()}` }>{method}</span>
    <span class="title">{title}</span>
</div>