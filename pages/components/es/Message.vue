<template>
  <section id="message" class="section section-lg pt-lg-0">
    <div class="container">
      <div class="alert alert-info" role="alert">
        <b>Hospital México y COVID-19</b>
      </div>
      <div class="row justify-content-center">
        <div class="col-lg-12">
          <div class="row row-grid align-items-center">
            <div class="col-lg-12">
              <card class="border-0" hover shadow body-classes="py-5">
                <div class="row">
                  <div class="col-md-8">
                    <h6 class="text-primary text-uppercase">
                      Hospital México permanece abierto
                    </h6>
                    <p class="description mt-3">
                      Los Estados Unidos ha limitado de manera temporal los
                      cruces fronterizos por tierra con Canadá y México
                      únicamente a “viajes esenciales”. Esta acción no prohíbe a
                      los ciudadanos estadounidenses y residentes permanentes
                      que regresen a los Estados Unidos.
                    </p>
                    <div class="text-right">
                      <a href="https://mx.usembassy.gov/wha-press-guidance/"
                        >Embajada de Estados Unidos</a
                      >
                    </div>

                    <p class="description mt-3">
                      Hospital México está tomando todas las medidas necesarias
                      para garantizar su seguridad y bienestar. Por favor
                      llámenos a
                      <a
                        href="tel:6646836363"
                        target="_blank"
                        rel="noopener"
                        data-toggle="tooltip"
                        title="Llámenos"
                        >664 683 6363</a
                      >
                      en caso de tener alguna duda o pregunta.
                    </p>
                  </div>
                  <div class="col-md-4">
                    <img
                      v-lazy="'/img/tourism/hm-tijuana.jpg'"
                      class="rounded-square img-center img-fluid shadow"
                      style="height:300px"
                    />
                  </div>
                </div>
              </card>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
