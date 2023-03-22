<script>
import Product from './components/Product.vue';

  export default {
    name: 'app',
    components: { 
      Product
     },
    data () {
      return {
        
      }
    }
  }
</script>

<template>
  <main>
    <section class="product">
     
      <Product />
    </section>
  </main>
</template>

<style>

</style>
