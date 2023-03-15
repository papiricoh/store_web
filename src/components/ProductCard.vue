<script>
export default {
  data() {
    return {
      product_name: "Example Name",
      img_route: "https://images.pexels.com/photos/991509/pexels-photo-991509.jpeg",
      product_price: 100.5,
    }
  },
}
</script>

<template>
    <div class="card">
        <div class="card_img"><img width="260" :src="img_route" :alt="product_name"></div>
        <div class="card_title">{{ product_name }}</div>
        <div class="card_price">{{ product_price.toLocaleString() }}€</div>
    </div>
</template>