<template>
  <section class="section">
    <div class="container">
      <div class="row row-grid align-items-center">
        <div class="col-lg-12">
          <card class="border-0" hover shadow body-classes="py-5">
            <div class="row text-justify">
              <!-- <div class="col-md-4">
                <h6 class="text-primary text-uppercase">
                  Cada vez más personas se atienden fuera de Estados Unidos
                </h6>
                <p class="description mt-3">
                  De acuerdo a la “Encuesta 2017 de los tiempos de espera de
                  citas médicas y las tasas de aceptación de Medicare y
                  Medicaid”, los pacientes esperan un promedio de 24 días para
                  programar una cita de primera vez con un médico; esto
                  representa un incremento de 30% comparado con el año 2014.
                </p>
              </div> -->
              <div class="col-md-12">
                <img
                  v-lazy="'/img/videoconsulta/PublicidadVideoConsulta-min.png'"
                  class="rounded-square img-center img-fluid"
                  alt="HM Tijuana"
                />
              </div>
            </div>
          </card>
        </div>
      </div>
      <div class="row row-grid align-items-center">
        <div class="col-md-6 order-md-1">
          <div class="pr-md-5">
            <icon
              name="fa fa-hospital-o"
              class="mb-5"
              size="lg"
              type="success"
              shadow
              rounded
            ></icon>
            <h1>Atención médica a su alcance por más de 25 años.</h1>
            <ul class="list-unstyled mt-5">
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-clock-o"
                  ></badge>
                  <h6 class="mb-0">
                    Atención médica y cirugía inmediata en Hospital México.
                  </h6>
                </div>
              </li>
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-calendar-times-o"
                  ></badge>
                  <h6 class="mb-0">No se requiere una cita.</h6>
                </div>
              </li>
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-usd"
                  ></badge>
                  <h6 class="mb-0">
                    Ahorre hasta un 70% del costo de cirugías en E.U.
                  </h6>
                </div>
              </li>
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-bus"
                  ></badge>
                  <h6 class="mb-0">
                    Servicio de transporte de San Diego a Tijuana.
                  </h6>
                </div>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-md-6 order-md-2">
          <img
            v-lazy="'/img/slider/HM-main-cirugias-min.jpg'"
            class="img-fluid"
            alt="Surgeries image"
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Descripcion'
}
</script>
