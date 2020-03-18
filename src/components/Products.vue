<template>
   
  <div class="col mb-4">
    <div class="card">
      <img :src="listproducts.image" height="250" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{listproducts.name}}</h5>

        <p>&#8358; {{listproducts.price}}</p>
        <button primary-success>Buy Now</button>
      </div>
    </div>

  
</div>
</template>

<script>
export default {
    props: ["listproducts"]
}
</script>