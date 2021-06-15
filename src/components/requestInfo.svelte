<svelte:options tag="request-info" />

<script>
    import RequestTitle from "./requestTitle.svelte"
    import RequestUrl from "./requestUrl.svelte"
    import RequestDescription from "./requestDescription.svelte"
    import RequestButton from "./sendRequesButton.svelte"

    // export let requestObj = {
    //     method: "POST",
    //     title: "Generate Access Token",
    //     url: "https://api.imgur.com/oauth2/token",
    //     description: "Given a user's refresh token, this endpoint generates an access token."
    // }

    // export let requestObj = {
    //     method: "GET",
    //     title: "Comment",
    //     url: "https://api.imgur.com/3/comment/{{commentId}}",
    //     description: "Get information about a specific comment."
    // }
    export let method = "GET";
    export let title = "Comment"
    export let url = "https://api.imgur.com/3/comment/123";
    export let description = "Get information about a specific comment."
</script>

<style>
    .container {
        border: 1px solid black;
        width: 50%;
        margin: 30px;
    }
</style>

<div class="container">
    <RequestTitle method={method} title={title}/>
    <RequestUrl  url={url}/>
    <RequestDescription description={description}/>
    <RequestButton />

    <!-- <RequestTitle method={requestObj.method} title={requestObj.title}/>
    <RequestUrl  url={requestObj.url}/>
    <RequestDescription description={requestObj.description}/>
    <RequestButton /> -->
</div>
