<script>
  import Carousel from "@beyonk/svelte-carousel";
  import { ChevronLeftIcon, ChevronRightIcon } from "svelte-feather-icons";

  export let gallery = false;
</script>

<style>
  .control :global(svg) {
    width: 100%;
    height: 100%;
    color: #fff;
    border: 2px solid #fff;
    border-radius: 32px;
  }

  .slide-content {
    overflow: hidden;
    border-radius: 8px;
    margin: 4px;
  }

  .slide-content img {
    max-width: 100%;
  }
</style>

{#if gallery}
  <Carousel perPage={{ 992: 3, 576: 2 }}>
    <span class="control" slot="left-control">
      <ChevronLeftIcon />
    </span>
    <span class="control" slot="right-control">
      <ChevronRightIcon />
    </span>
    {#each gallery as pic}
      <div class="slide-content">
        <img src={pic} alt="" />
      </div>
    {/each}
  </Carousel>
{/if}
