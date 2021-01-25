<!-- Article.vue -->
<template>
  <div class="container">
    <FormRegister></FormRegister>
  </div>
</template>
<script>
import FormRegister from '../components/register/FormRegister'
export default {
  layout: 'SimpleLayout',
  name: 'Register',
  components: { FormRegister },
  data() {
    return {
      title: 'Hospital México​ - Aviso de consulta',
      description:
        'Favor de llenar los siguientes datos para agilizar el proceso de su cita.'
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Registro',
          name: 'Aviso de consulta, Hospital Mexico​ Tijuana',
          content: 'Consulta, Hospital, Mexico​, Tijuana'
        }
      ]
    }
  }
}
</script>
