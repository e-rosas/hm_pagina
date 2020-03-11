<!-- Article.vue -->
<template>
  <div class="container">
    <FormRegister></FormRegister>
  </div>
</template>
<script>
import FormRegister from './components/register/FormRegister'
export default {
  layout: 'App',
  name: 'Register',
  components: { FormRegister },
  data() {
    return {
      title: 'Hospital México​ - Aviso de consulta'
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Registro',
          name: 'Aviso de consulta, Hospital México​ Tijuana',
          content: 'Consulta, Hospital, México​, Tijuana'
        }
      ]
    }
  }
}
</script>
