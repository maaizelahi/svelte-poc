<svelte:options tag="my-counter" />

<script>
	export let count = 0;
	let countError = false;

	function inc() {
		count++;
	}

	function dec() {
		count--;
	}
	$: {
		console.log(`Reactive count is ${count}`);
		if(count < 0) {
			countError = true;
		} else {
			countError = false;
		}
	}
</script>

<style>
	* {
		font-size: 200%;
	}

	span {
		width: 4rem;
		display: inline-block;
		text-align: center;
	}

	button {
		width: 64px;
		height: 64px;
		border: none;
		border-radius: 10px;
		background-color: seagreen;
		color: white;
	}
	.error {
		color: red;
	}
</style>

<button on:click={dec}>
	-
</button>
<span>{count}</span>
<button on:click={inc}>
	+
</button>
{#if countError}
	<div class="error">Count should be positive</div>
{/if}