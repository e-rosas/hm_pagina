<template>
  <div class="row justify-content-center">
    <div class="col-lg-12">
      <img
        v-lazy="'/img/promo/HM-promo-Background-min.jpg'"
        class="img-fluid"
        alt="Promo image"
      />
    </div>
    <div class="col-lg-12 mt--300">
      <card gradient="secondary" shadow body-classes="p-lg-5">
        <h1 class="mt-0">
          Detalles de la promoción
        </h1>
        <div>
          <b-form @submit="onSubmit">
            <div class="row">
              <div class="col-lg-8">
                <b-form-group
                  id="input-group-name"
                  label="Nombre completo"
                  label-for="input-name"
                  :state="$v.form.name.$invalid"
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
              <div class="col-lg-4">
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
              <div class="col-lg-8">
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
              <div class="col-lg-4">
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
              <div class="col-lg-4">
                <b-form-group label="¿Cuenta con aseguranza?">
                  <b-form-radio-group v-model="form.insured" :options="options">
                  </b-form-radio-group>
                </b-form-group>
              </div>
              <div class="col-lg-8">
                <b-form-group
                  id="input-group-city"
                  label="Ciudad donde vive"
                  label-for="input-city"
                  :state="!$v.form.city.$invalid"
                >
                  <b-form-input
                    id="input-city"
                    v-model="form.city"
                    :state="!$v.form.city.$invalid"
                    required
                    placeholder="Ciudad"
                  ></b-form-input>
                  <div v-if="!$v.form.city.required" class="error">
                    Nombre de la ciudad es requerido
                  </div>
                </b-form-group>
              </div>
            </div>
            <div class="row">
              <div class="col-lg-12">
                <b-form-group
                  id="input-group-relatives"
                  label="Nombre completo de familiares que desea incluir"
                  label-for="input-relatives"
                >
                  <b-form-textarea
                    id="input-cooments"
                    v-model="form.relatives"
                    rows="3"
                    max-rows="6"
                  ></b-form-textarea>
                </b-form-group>
              </div>
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
        phone: '',
        birth_date: null,
        insured: 0,
        city: '',
        relatives: ''
      },
      options: [
        { text: 'Si', value: 1 },
        { text: 'No', value: 0 }
      ]
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      const currentObj = this
      this.$v.$touch()
      if (this.$v.$invalid) {
        this.submitStatus = 'ERROR'
      } else {
        // do your submit logic here
        this.$axios
          .post('http://promociones-api.hospitalmexico.org/api/register', {
            name: this.form.name,
            birth_date: this.form.birth_date,
            phone_number: this.form.phone,
            email: this.form.email,
            insured: this.form.insured,
            city: this.form.city,
            relatives: this.form.relatives
          })

          .then(function(response) {
            currentObj.output = response.data
          })

          .catch(function(error) {
            currentObj.output = error
          })
        this.submitStatus = 'PENDING'
        setTimeout(() => {
          this.submitStatus = 'OK'
        }, 500)
      }
    }
  },
  validations: {
    form: {
      name: { required, minLength: minLength(6) },
      city: { required },
      email: { required, email },
      phone: { required, minLength: minLength(7) },
      birth_date: { required }
    }
  }
}
</script>
