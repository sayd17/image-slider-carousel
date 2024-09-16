<script>
    import Carousel from "svelte-carousel";
    import CustomDot from "./CustomDot.svelte";
    export let images;
    let carousel;
    let hidden = true;

    const handleNextClick = () => {
        carousel.goToNext();
    }
    
    const handlePrevClick = () => {
        carousel.goToPrev();
    }
</script>

<Carousel 
    pauseOnFocus
    autoplay
    autoplayDuration={3000}
    autoplayProgressVisible
    bind:this={carousel}
    let:loaded
    let:currentPageIndex
    let:pagesCount
    let:showPage
    
>
    <button on:mouseenter={() => hidden = false} on:mouseleave={() => hidden=true} slot="prev" on:click={handlePrevClick} class={`${hidden ? 'hide-element' : ''} custom-button left-radius`}>
        
        <img src="/assets/arrow-left.png" alt="left arrow" width="15px" height="15px" />
    
    </button>

    <div slot="dots">

        {#each  Array(pagesCount) as _, pageIndex (pageIndex)}
        
            <CustomDot on:click={showPage(pageIndex)} active={currentPageIndex === pageIndex}>
                {pageIndex}
            </CustomDot>

        {/each}
      
    </div>

    {#each images as image, index}

        <div on:mouseenter={() => hidden = false} on:mouseleave={() => hidden=true}>

            <!-- lazy loading -->
            {#if loaded.includes(index)}
            
                <img src={image.src} alt={image.desc} width="100%" height="400" />
            
            {/if}
        </div>
    {/each}

    <button  on:mouseenter={() => hidden = false} on:mouseleave={() => hidden=true} slot="next" on:click={handleNextClick} class={`${hidden ? 'hide-element' : ''} custom-button right-radius`}>
        
        <img src="/assets/arrow-right.png" alt="right arrow" width="15px" height="15px" />
    
    </button>

</Carousel>

<style>
    div {
        text-align: center;
    }
    .custom-button {
        background-color: var(--button-bg-color);
        color: var(--button-text-color);
        padding: var(--button-padding);
        font-size: var(--button-font-size);
        border: var(--button-border);
        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    .hide-element {
        visibility: hidden;
    }
    .left-radius {
        border-top-left-radius: var(--border-top-left-radius);
        border-bottom-left-radius: var(--border-bottom-left-radius);
    }
    .right-radius {
        border-top-right-radius: var(--border-top-right-radius);
        border-bottom-right-radius: var(--border-bottom-right-radius);
    }

  .custom-button:hover {
    background-color: var(--button-hover-bg-color);
  }
</style>