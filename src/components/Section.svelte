<script>
  export let id;
  export let light = false;
</script>

<section class="page-section {light ? 'bg-light' : ''}" {id}>
  <div class="container">
    <slot />
  </div>
</section>
