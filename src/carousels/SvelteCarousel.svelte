<script>
    import Carousel from "svelte-carousel";
    export let images;
</script>

<Carousel 
    pauseOnFocus
    autoplay
    autoplayDuration={2000}
    autoplayProgressVisible
>
    {#each images as image, index (index)}
    <div><img src={image.src} alt={image.desc} width="1000" height="500" /></div>
    {/each}
</Carousel>