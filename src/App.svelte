<script>
	import Counter from "./components/counter.svelte"
	// import Counter from "./components/"
	import RequestInfo from "./components/requestInfo.svelte"
	export let count;

	let requestObj1 = {
        method: "POST",
        title: "Generate Access Token",
        url: "https://api.imgur.com/oauth2/token",
        description: "Given a user's refresh token, this endpoint generates an access token."
    }
	let requestObj2 = {
        method: "GET",
        title: "Comment",
        url: "https://api.imgur.com/3/comment/{{commentId}}",
        description: "Get information about a specific comment."
    }
</script>

<!-- <Counter count={count} /> -->
<!-- <RequestInfo requestObj={requestObj1}/> -->
<!-- <RequestInfo requestObj={requestObj2}/> -->
<!-- <request-info /> -->

