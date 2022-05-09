<template>
<div class="container">
  <h1 class="m-3">Formulario de Contacto</h1>
  <FormContact />
</div>
</template>

<script>
// @ is an alias to /src
import FormContact from '@/components/FormContact.vue'

export default {
  name: 'ContactView',
  components: {
    FormContact
  }
}
</script>
