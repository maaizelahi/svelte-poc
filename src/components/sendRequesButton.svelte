<svelte:options tag="request-btn" />

<script>
    function sendRequest() {
        console.log("Maaiz send Request Clicked");
    }
    function changeUrl() {
        console.log("Maaiz ChangeUrl Clicked");
    }
</script>

<style>
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

<button on:click={sendRequest}>
    Send Request
</button>
<button on:click={sendRequest}>
    Change url
</button>