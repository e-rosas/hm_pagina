<template>
  <div>
    <b-form v-if="show" @submit="onSubmit" @reset="onReset">
      <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          required
          placeholder="Enter name"
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-1"
        label="Email address:"
        label-for="input-1"
        description="We'll never share your email with anyone else."
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          required
          placeholder="Enter your email"
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-phone"
        label="Phone number:"
        label-for="input-phone"
      >
        <b-form-input
          id="input-phone"
          v-model="form.phone_number"
          required
          placeholder="Enter your phone number"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Birth date:" label-for="input-3">
        <b-form-input
          id="input-3"
          v-model="form.date"
          type="date"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-4" label="Insured">
        <b-form-radio v-model="form.insured" name="insured" value="1"
          >Yes</b-form-radio
        >
        <b-form-radio v-model="form.insured" name="insured" value="0"
          >No</b-form-radio
        >
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: '',
        name: '',
        birth_date: '',
        phone_number: '',
        insured: 0
      },
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
      const currentObj = this

      this.$axios
        .post('http://localhost:8000/register', {
          name: this.name,
          birth_date: this.birth_date,
          phone_number: this.phone_number,
          email: this.email,
          insured: this.insured
        })

        .then(function(response) {
          currentObj.output = response.data
        })

        .catch(function(error) {
          currentObj.output = error
        })
    },
    onReset(evt) {
      evt.preventDefault()
      // Reset our form values
      this.form.email = ''
      this.form.name = ''
      this.form.birth_date = ''
      this.form.insured = 0
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>
