<script>
	import SvelteCarousel from './components/SvelteCarousel.svelte'

	const images = [
		{
			src: 'https://plus.unsplash.com/premium_photo-1681584472513-9f1f33f3928a?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
            desc: 'Inspiration board'
        },
		{
			src: 'https://plus.unsplash.com/premium_photo-1681680199227-b456408ae2f9?q=80&w=1413&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
            desc: 'Art Mockup'
        },
		{
			src: 'https://plus.unsplash.com/premium_photo-1681680198696-7bb0b3fdda0d?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
            desc: 'Paper-background'
        },
		{
			src: 'https://plus.unsplash.com/premium_photo-1722945688629-0d31e4850b24?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
            desc: 'Fishes walmate frame'
        },
		{
			src: 'https://plus.unsplash.com/premium_photo-1664391914821-29ee0b3d98ee?q=80&w=1510&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
            desc: 'Interior design'
        },
		
	];

</script>

<main>
	<h1>Image Carousel</h1>
	<SvelteCarousel images={images} />

</main>

<style>
	h1 {
		text-align: center;
		text-decoration: underline;
	}

</style>