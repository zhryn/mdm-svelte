<script>
  export let name;
  export let img;
</script>

<div class="col-md-4 col-sm-6 product-item">
  <div class="product-link">
    <div class="product-hover">
      <div class="product-hover-content" />
    </div>
    <img class="img-fluid" src={img} alt="" />
  </div>
  <div class="product-caption">
    <h4>{name}</h4>
  </div>
</div>
