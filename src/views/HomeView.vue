<template>
  <div class="home">
    <h1>Home</h1>
      <div class="splash-container">
          <div class="splash">
            <h1>Splendid Food</h1>
          </div>
      </div>

    <main class="wrapper">
      <h2>Recommended</h2>
      <div class="recommended">
        <ProductCard
        v-for="(product, index) in inventory.slice(0,3)"
        :key="product.id"
        :index="index"
        :product="product"
        :addToCart="addToCart"
        class="card"
        />
      </div>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src'=
import ProductCard from '../components/ProductCard.vue'
export default {
  name: 'HomeView',
  props: (['inventory', 'addToCart']),
  components: {
    ProductCard
  }
}
</script>
