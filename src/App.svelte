<script>
	export let createdMeal;
</script>

<main>
	{#if !createdMeal}
		<h1>What do you want to eat today?</h1>
		<button on:click={() => createdMeal = true}>Generate Meal</button>
	{:else}
		<h1><strong>Food.</strong></h1>
	{/if}

	<footer>Created by <a href="//www.brianfran.co">Brian Franco.</a></footer>
</main>

<style>
	:global(body) {
		background: #f79420;
		display: grid;
		place-content: center;
	}

	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}

	h1 {
		color: white;
		text-transform: uppercase;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		font-size: 6em;
		font-weight: 100;
	}
	
	@media screen and (max-width: 500px) {
		h1 { font-size: 3em; }	
	}

	button {
		background: #f1522e;
		border: 0 none;
		color: white;
		padding: 10px 20px;
	}

	button:active {
		background: #a53016;
	}

	footer {
		line-height: 40px;
		position: fixed;
		text-align: center;
		bottom: 0; left: 0;
		width: 100%;
	}

	footer a {
		color: #f1522e;
	}
</style>
