<script>
	let firstName = 'Mohamed';
	let lastName = 'Hamidi';
	let color = 'blue';
	$: name = firstName + ' ' + lastName
	const toggleColor = () => { 
		color === 'blue' ? color = 'purple' : color = 'blue'
		}
</script>

<main>
	<h1 style="color: {color}">Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<button on:click={toggleColor} >Click</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>