<template>
  <div class="row justify-content-center">
    <div class="col-lg-12">
      <card gradient="secondary" shadow body-classes="p-lg-5">
        <h4 class="mb-1">Promo</h4>
        <p class="mt-0">
          Texto
        </p>
        <div>
          <b-form @submit="onSubmit">
            <div class="row">
              <div class="col-lg-8 col-sm-6">
                <b-form-group
                  id="input-group-name"
                  label="Nombre completo"
                  label-for="input-name"
                  :state="!$v.form.name.$invalid"
                >
                  <b-form-input
                    id="input-name"
                    v-model="form.name"
                    :state="!$v.form.name.$invalid"
                    required
                    placeholder="Nombre completo"
                  ></b-form-input>
                  <div v-if="!$v.form.name.required" class="error">
                    Nombre completo es requerido
                  </div>
                  <div v-if="!$v.form.name.minLength" class="error">
                    Nombre debe tener al menos
                    {{ $v.form.name.$params.minLength.min }} letras.
                  </div>
                </b-form-group>
              </div>
              <div class="col-lg-4 col-sm-6">
                <b-form-group
                  id="input-group-phone"
                  label="Teléfono"
                  label-for="input-phone"
                  :state="!$v.form.phone.$invalid"
                >
                  <b-form-input
                    id="input-phone"
                    v-model="form.phone"
                    :state="!$v.form.phone.$invalid"
                    required
                    placeholder="Número de teléfono"
                  ></b-form-input>
                  <div v-if="!$v.form.phone.required" class="error">
                    Número de teléfono es requerido
                  </div>
                  <div v-if="!$v.form.phone.minLength" class="error">
                    Número de teléfono debe tener al menos
                    {{ $v.form.phone.$params.minLength.min }} digitos.
                  </div>
                </b-form-group>
              </div>
            </div>
            <div class="row">
              <div class="col-lg-8 col-sm-6">
                <b-form-group
                  id="input-group-email"
                  label="E-mail"
                  label-for="input-email"
                  :state="!$v.form.email.$invalid"
                >
                  <b-form-input
                    id="input-email"
                    v-model="form.email"
                    type="email"
                    :state="!$v.form.email.$invalid"
                    required
                    placeholder="Correo electrónico"
                  ></b-form-input>
                  <div v-if="!$v.form.email.required" class="error">
                    Correo es requerido
                  </div>
                  <div v-if="!$v.form.email.email" class="error">
                    Por favor ingrese un correo válido
                  </div>
                </b-form-group>
              </div>
              <div class="col-lg-4 col-sm-6">
                <b-form-group
                  id="input-group-bith-date"
                  label="Fecha de nacimiento"
                  label-for="input-birth_date"
                  :state="!$v.form.birth_date.$invalid"
                >
                  <b-form-datepicker
                    id="input-birth_date"
                    v-model="form.birth_date"
                    :state="!$v.form.birth_date.$invalid"
                    required
                    :max="todayDate"
                    placeholder="Fecha de nacimiento"
                    class="mb-2"
                  ></b-form-datepicker>
                  <div v-if="!$v.form.birth_date.required" class="error">
                    Fecha de nacimiento es requerida
                  </div>
                </b-form-group>
              </div>
            </div>
            <div class="row">
              <div class="col-lg-3 col-sm-6">
                <b-form-group label="¿Cuenta con aseguranza?">
                  <b-form-radio-group v-model="form.insured" :options="options">
                  </b-form-radio-group>
                </b-form-group>
              </div>
              <div class="col-lg-9 col-sm-6">
                <b-form-group label="Familiares que desea incluir: ">
                  <b-form-input v-model="count" type="number"></b-form-input>
                </b-form-group>
              </div>
            </div>
            <div class="row">
              <ul v-for="h in count" :key="h">
                <li>
                  <b-form-input type="text"></b-form-input>
                </li>
              </ul>
            </div>

            <b-button block type="submit" variant="primary">Enviar</b-button>
            <p v-if="submitStatus === 'OK'" class="typo__p">
              !Gracias!
            </p>
            <p v-if="submitStatus === 'ERROR'" class="typo__p">
              Por favor complete correctamente los campos requeridos.
            </p>
            <p v-if="submitStatus === 'PENDING'" class="typo__p">
              Enviando...
            </p>
          </b-form>
        </div>
      </card>
    </div>
  </div>
</template>
<script>
import { required, minLength, email } from 'vuelidate/lib/validators'
export default {
  data() {
    const now = new Date()
    const today = new Date(now.getFullYear(), now.getMonth(), now.getDate())
    return {
      todayDate: today,
      submitStatus: null,
      form: {
        email: '',
        name: '',
        city: '',
        phone: '',
        birth_date: null,
        appointment_date: null,
        last_appointment: null,
        motive: null,
        comments: ''
      },
      count: 0,
      options: [
        { text: 'Si', value: 1 },
        { text: 'No', value: 0 }
      ]
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
  },
  validations: {
    form: {
      name: { required, minLength: minLength(4) },
      city: { required },
      email: { required, email },
      phone: { required, minLength: minLength(7) },
      birth_date: { required },
      appointment_date: { required },
      last_appointment: { required },
      motive: { required }
    }
  }
}
</script>
