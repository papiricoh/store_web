<script setup>
import ProductCard from './ProductCard.vue';
</script>

<script>
export default {
  data() {
    return {
      debug_number_of_cards: 4,
    }
  },
}
</script>

<template>
  <div class="flex_column">
    <div class="hero">
      <div id="main_title">Scylla</div>
      <div class="title" id="main_subtitle">Hypebeast</div>
    </div>
    <div class="section">
      <div>
        <ProductCard />
      </div>
      <div>
        <ProductCard />
      </div>
      <div>
        <ProductCard />
      </div>
    </div>
  </div>
</template>
