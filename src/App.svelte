<script>
    import Carousel from './carousels/SvelteCarousel.svelte' 
	import Practice from './carousels/Practice.svelte';
</script>

<main>
    <h1>Svelte-carousel</h1>
    <Carousel />
	<Practice />
</main>


<style>
	main {
		text-align: center;
		padding: 1em;
		/* max-width: 600px; */
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
</style>