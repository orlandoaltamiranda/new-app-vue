<template>

<div class="container">
    <form class="row g-3">
  <div class="col-12">
    <label for="inputAddress" class="form-label">Email:</label>
    <input type="text" class="form-control" id="inputAddress" placeholder="Ingrese su correo">
  </div>
  <div class="col-12">
    <label for="password" class="form-label">Contraseña</label>
    <input type="password" class="form-control" id="password" placeholder="Ingrese su contraseña">
  </div>
  <div class="col-12">
    <button type="submit" class="btn btn-success mb-5">Iniciar Sesión</button>
  </div>
</form>
</div>
  
</template>

<script>
export default {
  name: 'LoginForm',
}
</script>

<style>

</style>