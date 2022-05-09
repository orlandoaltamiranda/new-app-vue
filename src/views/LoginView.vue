<template>
<div class="container">
  <h1 class="m-3">Iniciar Sesión</h1>
  <login-form />
</div>
</template>

<script>
// @ is an alias to /src
import LoginForm from '@/components/LoginForm.vue'

export default {
  name: 'LoginView',
  components: {
    LoginForm
  }
}
</script>