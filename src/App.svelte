<script>
	import SvelteCarousel from './carousels/SvelteCarousel.svelte'

	const images = [
		{
			src: 'https://media.istockphoto.com/id/1265024528/photo/no-better-adventure-buddy.jpg?s=1024x1024&w=is&k=20&c=tObIEgQAXKm_OQwuZ0xNXA-U0QMXx2Okgm_L6Ew9Ygk=',
            desc: 'Adventure buddy'
		},
		{
			src: 'https://media.istockphoto.com/id/1322104312/photo/freedom-chains-that-transform-into-birds-charge-concept.jpg?s=1024x1024&w=is&k=20&c=CoqB4hDuRFuxxEZ4Fu84uhLDftgeyAtl8TXEQq-JdtM=',
            desc: 'Freedom chain'
        },
		{
			src: 'https://media.istockphoto.com/id/121199853/photo/closeup-of-guy-working-on-a-laptop-indoor.jpg?s=1024x1024&w=is&k=20&c=0uAngvDAolHrh_LUWorV6ZJD5AVO6g2tfavtw9PPHYQ=',
            desc: 'Working on a laptop indoor'
        }
	];

</script>

<main>
	
	<SvelteCarousel images={images} />

</main>

<style>

</style>