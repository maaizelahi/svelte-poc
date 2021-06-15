<svelte:options tag="request-info-full" />

<script>
    import RequestTitle from "./requestTitle.svelte"
    import RequestUrl from "./requestUrl.svelte"
    import RequestDescription from "./requestDescription.svelte"
    import RequestButton from "./sendRequesButton.svelte"

    // export let requestobj = {
    //     method: "POST",
    //     title: "Generate Access Token",
    //     url: "https://api.imgur.com/oauth2/token",
    //     description: "Given a user's refresh token, this endpoint generates an access token."
    // }

    // export let requestobj = {
    //     method: "GET",
    //     title: "Comment",
    //     url: "https://api.imgur.com/3/comment/{{commentId}}",
    //     description: "Get information about a specific comment."
    // }
    export let method = "GET";
    export let title = "Comment"
    export let url = "https://api.imgur.com/3/comment/123";
    export let description = "Get information about a specific comment."

    // $: {
    //     // console.log(JSON.parse(requestobj));
    //     requestobj = typeof requestobj === 'string' ? JSON.parse(requestobj) : requestobj;
    // }
    
    function sendRequest() {
        console.log("Maaiz send Request Clicked");
    }
</script>

<style>
    .container {
        border: 1px solid black;
        width: 50%;
        margin: 30px;
    }
    .title-container {
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
    .url-container {
        margin: 5px 12px 15px;
        padding: 6px 10px;
        background-color: rgb(248, 248, 248);
        border: 1px solid #ccc;
        font-size: 12px;
    }
    .desc-container {
        padding: 0px 12px 10px;
    }
    button {
        font-size: .8rem;
		width: 100px;
		height: 40px;
		border: none;
		border-radius: 5px;
		background-color: #F26B3A;
		color: white;
        margin: 12px;
	}
</style>

<div class="container">
    <div class="title-container">
        <span class={`method ${method.toLowerCase()}` }>{method}</span>
        <span class="title">{title}</span>
    </div>
    <div class="url-container">{url}</div>
    <div class="desc-container">{description}</div>
    <button on:click={sendRequest}>
        Send Request
    </button>
    <!-- Component with requestObj - removed it as there was problem passing it from web component -->
    <!-- <div class="title-container">
        <span class={`method ${requestobj.method.toLowerCase()}` }>{requestobj.method}</span>
        <span class="title">{requestobj.title}</span>
    </div>
    <div class="url-container">{requestobj.url}</div>
    <div class="desc-container">{requestobj.description}</div>
    <button on:click={sendRequest}>
        Send Request
    </button> -->
    <!-- <RequestTitle method={requestobj.method} title={requestobj.title}/>
    <RequestUrl  url={requestobj.url}/>
    <RequestDescription description={requestobj.description}/>
    <RequestButton /> -->
</div>