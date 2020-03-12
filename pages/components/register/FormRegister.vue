<template>
  <section class="section section-lg section-contact-us">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-12">
          <card gradient="secondary" shadow body-classes="p-lg-5">
            <h4 class="mb-1">Aviso de consulta</h4>
            <p class="mt-0">
              Para brindarle un mejor servicio favor de avisarnos que día planea
              venir, se atiende en el orden en que llega al hospital.
            </p>
            <p class="mt-0">
              (Sólo aplica para pacientes que ya tienen expediente en Hospital
              México)
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
                  <div class="col-lg-4 col-sm-6">
                    <b-form-group
                      id="input-group-appointment_date"
                      label="Fecha de próxima consulta"
                      label-for="input-appointment_date"
                      :state="!$v.form.appointment_date.$invalid"
                    >
                      <b-form-datepicker
                        id="input-appointment_date"
                        v-model="form.appointment_date"
                        :state="!$v.form.appointment_date.$invalid"
                        required
                        today-button
                        close-button
                        :min="todayDate"
                        placeholder="Fecha de próxima consulta"
                        class="mb-2"
                      ></b-form-datepicker>
                      <div
                        v-if="!$v.form.appointment_date.required"
                        class="error"
                      >
                        Fecha de próxima consulta es requerida
                      </div>
                    </b-form-group>
                  </div>
                  <div class="col-lg-4 col-sm-6">
                    <b-form-group
                      id="input-group-last_appointment"
                      label="Fecha de última consulta"
                      label-for="input-last_appointment"
                      :state="!$v.form.last_appointment.$invalid"
                    >
                      <b-form-select
                        id="input-last_appointment"
                        v-model="form.last_appointment"
                        :options="dates"
                        :state="!$v.form.last_appointment.$invalid"
                        required
                      ></b-form-select>
                      <div
                        v-if="!$v.form.last_appointment.required"
                        class="error"
                      >
                        Fecha de última consulta es requerida
                      </div>
                    </b-form-group>
                  </div>
                </div>
                <div class="row">
                  <div class="col-lg-12 col-sm-6">
                    <b-form-group
                      id="input-group-motive"
                      label="Motivo de consulta"
                      label-for="input-motive"
                      :state="!$v.form.motive.$invalid"
                    >
                      <b-form-select
                        id="input-motive"
                        v-model="form.motive"
                        :state="!$v.form.motive.$invalid"
                        :options="motives"
                        required
                      ></b-form-select>
                      <div v-if="!$v.form.motive.required" class="error">
                        Motivo consulta es requerido
                      </div>
                    </b-form-group>
                  </div>
                </div>
                <div class="row">
                  <div class="col-lg-12 col-sm-6">
                    <b-form-group
                      id="input-group-comments"
                      label="Comentarios/Padecimiento"
                      label-for="input-comments"
                    >
                      <b-form-textarea
                        id="input-comments"
                        v-model="form.comments"
                        placeholder="Comentarios..."
                        rows="3"
                        max-rows="6"
                      ></b-form-textarea>
                    </b-form-group>
                  </div>
                </div>

                <b-button block type="submit" variant="primary"
                  >Enviar</b-button
                >
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
    </div>
  </section>
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
      dates: [
        { text: 'Seleccione una', value: null },
        'Hace un mes',
        'Hace tres meses',
        'Hace 6 meses',
        'Más de 6 meses'
      ],
      motives: [
        { text: 'Seleccione una', value: null },
        'CONSULTA DE CONTROL (MÉDICO GENERAL)',
        'CONSULTA DENTAL'
      ]
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      this.$v.$touch()
      if (this.$v.$invalid) {
        this.submitStatus = 'ERROR'
      } else {
        // do your submit logic here
        this.submitStatus = 'PENDING'
        setTimeout(() => {
          this.submitStatus = 'OK'
        }, 500)
      }
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
