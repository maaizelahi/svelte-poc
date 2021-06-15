<svelte:options tag="request-description" />

<script>
    export let description = "Given a user's refresh token, this endpoint generates an access token."
</script>

<style>
    .container {
        padding: 0px 12px 10px;
    }
</style>

<div class="container">{description}</div>