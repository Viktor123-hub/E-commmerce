<template>
  <div class="cart-item">
    <div class="p-2 d-flex justify-content-between align-items-center">

      <div class="d-flex align-items-center">
        <img :src="item.product.image" alt="" class="img-fluid image-width">
        <div>
          <div><strong>{{ item.product.name }}</strong></div>
          <div><small>{{ item.quantity }} x {{ item.product.price }}</small></div>
        </div>
      </div>

    </div>

    <div class="dropdown-divider"></div>
  </div>
</template>

<script>
export default {
  props: ['item']
}
</script>

<style>
.image-width {
  width: 90px;
}
</style>