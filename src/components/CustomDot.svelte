<script>
    /**
     * Indicates if dot is active
     */
    export let active = false
  </script>
  
  <button
    class="carousel-dot"
    class:carousel-dot_active={active}
    on:click
  >
  <slot></slot>
</button>
  
  <style>
    :root {
      --sc-dot-size: 20px;
      --sc-active-dot-size: 25px;
      --sc-dot-size-animation-time: 250ms;
    }
  
    .carousel-dot {
      text-align: center;
      background-color: var(--sc-color-rgb-light);
      border-radius: 50%;
      display: inline-block;
      opacity: 0.5;
      transition:
        opacity 100ms ease,
        height var(--sc-dot-size-animation-time) ease,
        width var(--sc-dot-size-animation-time) ease;
      cursor: pointer;
      height: var(--sc-dot-size);
      width: var(--sc-dot-size);
    }
    .carousel-dot:hover {
      opacity: 0.9;
    }
    .carousel-dot_active {
      opacity: 0.7;
      height: var(--sc-active-dot-size);
      width: var(--sc-active-dot-size);
    }
  </style>
  