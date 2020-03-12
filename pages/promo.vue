<template>
  <div class="container">
    <FormPromo></FormPromo>
  </div>
</template>

<script>
import FormPromo from './components/promo/FormPromo'

export default {
  components: { FormPromo },
  data() {
    return {
      form: {
        email: '',
        name: '',
        birth_date: '',
        phone_number: '',
        insured: 0
      }
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
      const currentObj = this

      this.$axios
        .post('http://promociones-api.hospitalmexico.org/api/register', {
          name: this.form.name,
          birth_date: this.form.birth_date,
          phone_number: this.form.phone_number,
          email: this.form.email,
          insured: this.form.insured
        })

        .then(function(response) {
          currentObj.output = response.data
        })

        .catch(function(error) {
          currentObj.output = error
        })
    }
  }
}
</script>
