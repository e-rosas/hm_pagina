<template>
  <section id="services" class="section section-lg pt-lg-0">
    <div class="container">
      <div class="row justify-content-center text-center mb-lg">
        <div class="col-lg-8">
          <h2 class="display-3">NUESTROS SERVICIOS</h2>
          <p class="lead text-muted">
            Estos son algunos de los servicios que ofrecemos:
          </p>
        </div>
      </div>
      <div class="row justify-content-center mt--100">
        <div class="col-md-6 col-lg-3 mb-5 mb-lg-0">
          <card class="border-0" hover shadow body-classes="py-5">
            <div class="px-6">
              <img
                v-lazy="'/img/services/servicio-dental-min.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Servicio dental"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Cirugía oral y maxilofacial, implantes dentales,
                    endodoncistas, ortodoncistas, periodoncistas.</small
                  >
                </h5>
              </div>
            </div>
          </card>
        </div>
        <div class="col-md-6 col-lg-3 mb-5 mb-lg-0">
          <card class="border-0" hover shadow body-classes="py-5">
            <div class="px-6">
              <img
                v-lazy="'/img/services/servicio-cirugias-min.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Servicio cirugias"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Amigdalas, apendice, vesícula, piedras en riñones,
                    extracción de útero, quiste de ovarios, hernias.</small
                  >
                </h5>
              </div>
            </div>
          </card>
        </div>
        <div class="col-md-6 col-lg-3 mb-5 mb-lg-0">
          <card class="border-0" hover shadow body-classes="py-5">
            <div class="px-6">
              <img
                v-lazy="'/img/services/servicio-especialistas-min.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Servicio especialistas"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Medicina Interna, dermatología, siquiatría, pediatría,
                    hematología, ginecología.</small
                  >
                </h5>
              </div>
            </div>
          </card>
        </div>
        <div class="col-md-6 col-lg-3 mb-5 mb-lg-0">
          <card class="border-0" hover shadow body-classes="py-5">
            <div class="px-6">
              <img
                v-lazy="'/img/services/servicio-laboratorio-min.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Servicio laboratorio"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Rayos-X, laboratorio y radio diagnóstico.</small
                  >
                </h5>
              </div>
            </div>
          </card>
        </div>
      </div>
    </div>
  </section>
</template>
