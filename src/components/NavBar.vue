<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="/home"><img src="https://www.el-parnasillo.com/miyazaki-ghibli/studio-ghibli.jpg" alt="" id="logo"></router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <router-link class="nav-link" to="/home">Inicio</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">Nosotros</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/favoritos">Favoritos</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contacto">Contacto</router-link>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <router-link class="btn btn-success" to="/">Iniciar Sesión</router-link>
      </form>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style>
#logo {
  width: 100px;
}

</style>