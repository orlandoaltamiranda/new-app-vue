<template>
  <div class="container">
    <h1 class="text-center m-3">Películas de Studio Ghibli</h1>
    <!-- <Search /> -->
    <CardProduct />
  </div>
</template>

<script>
// @ is an alias to /src
import CardProduct from '@/components/CardProduct.vue'
// import Search from '@/components/Search.vue'

export default {
  name: 'HomeView',
  components: {
    CardProduct,
    // Search,
  }
}
</script>
