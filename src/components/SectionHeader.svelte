<script>
  export let title = "";
  export let subtitle = "";
</script>

<div class="row">
  <div class="col-lg-12 text-center">
    <h2 class="section-heading text-uppercase">{title}</h2>
    {#if subtitle.length > 0}
      <h3 class="section-subheading text-muted">{subtitle}</h3>
    {/if}
  </div>
</div>
