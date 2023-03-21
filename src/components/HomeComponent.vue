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
      <ProductCard v-for="card in debug_number_of_cards"/>
    </div>
  </div>
</template>
