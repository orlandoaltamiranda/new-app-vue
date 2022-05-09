<template>
  <div class="container">
    <h1 class="text-center m-3">Mis Favoritos</h1>
    
    {{ this.favorites}}
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
  },

  props: ['favorites'],

  methods: {
    pp() {
      console.log(this.favorites)
    }
  }
}
</script>
