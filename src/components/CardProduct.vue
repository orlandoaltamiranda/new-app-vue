<template>
  <div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Buscar película" aria-label="Recipient's username" aria-describedby="button-addon2" v-model="busqueda">
</div>
  <div class="container mb-5">
    <div class="row d-flex justify-content-center">
      <div v-for="(item, index) in filtroBusqueda" :key="index" class="card m-3 shadow p-3 mb-5 bg-body rounded" style="width: 22rem;">
        <img v-bind:src="item.image" class="card-img-top" v-bind:alt="item.title">
        <div class="card-body">
          <h5 class="card-title fw-bold">{{ item.title }}</h5>
          <p class="card-text">{{ item.director }}</p>
          <a href="#" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal" v-on:click="showMovie(item)">Más detalles</a>
          <i class="fa-solid fa-heart btn btn-outline-danger m-2 fs-3" v-on:click="addFavorites(item)"></i>
          <i class="fa-solid fa-cart-plus btn btn-outline-success m-2 fs-3" v-on:click="addCar(item)"></i>
        </div>
      </div>
    </div>
  </div>
  <modal :movie='movie'> </modal>  
</template>

<script>
import Modal from '@/components/ModalMovie.vue'

export default {
  name: 'CardProduct',

  components: {
    Modal
  },
 
 data(){
    return {
      result: [],
      busqueda: '',
      favorites: [],
      movie: {},
      carShop: [],
      }
  },
  
  mounted(){
      fetch("https://ghibliapi.herokuapp.com/films/")
      .then(res => res.json())
      .then(data => this.result = data)
  },
  methods: {
    addFavorites(item){
    const repeat = this.favorites.some(personaje=>personaje == item);

      if (repeat) {
          console.log('Ya está en tus favoritos')
      } else {
          this.favorites.push(item);
      }
      console.log(this.favorites)
    },

    addCar(item){
    const repeat = this.carShop.some(personaje=>personaje == item);

      if (repeat) {
          console.log('Ya está en tus favoritos')
      } else {
          this.carShop.push(item);
      }
      console.log(this.carShop)
    },

    showMovie(object){
      this.movie = object
    },

    cambiarVista(tipo) {
      this.vista = !this.vista
    }
  },

  computed: {
    filtroBusqueda() {
      if (!this.busqueda) { return this.result }

      return this.result.filter( movie => movie.title.toLowerCase().includes(this.busqueda.toLowerCase()))
    }
  }
}
</script>

<style>

i:hover {
  color: black;
}

</style>