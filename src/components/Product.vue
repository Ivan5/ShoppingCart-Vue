<template lang="html">
  <div class="card my-5">
    <div class="card-body">
      <h5 class="text-center card-title">{{product.title }}</h5>
      <p class="text-center text-muted card-text display-4">${{Number(product.price).toFixed()}}</p>
      <button :disable="isInCart" class="btn btn-primary form-control" @click="$emit('add-to-cart',product)">{{isInCart ? 'Added to cart' : 'Add to Cart'}}</button>
    </div>
  </div>
</template>

<script>
export default {
  props:['product', 'isInCart']
}
</script>

<style lang="css">
</style>
