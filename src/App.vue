<template>
  <nav-bar />
  <router-view/>

  <footer-bar />
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css';

// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import FooterBar from '@/components/FooterBar.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    FooterBar,
  }
}
</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Macondo&display=swap');

* {
    font-family: 'Macondo', cursive;
    text-align: center;
}

h1 {
  font-size: 3rem;
}

h5 {
  font-size: 1.4rem;
}

p {
  font-size: 1.2rem;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
