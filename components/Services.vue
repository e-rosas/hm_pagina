<template>
  <section id="services" class="section section-lg pt-lg-0">
    <div class="container">
      <div class="row justify-content-center text-center mb-lg">
        <div class="col-lg-8">
          <h2 class="display-3">Our Services</h2>
          <p class="lead text-muted">
            These are some of the services we offer:
          </p>
        </div>
      </div>
      <div class="row justify-content-center mt--100">
        <div class="col-md-6 col-lg-3 mb-5 mb-lg-0">
          <card class="border-0" hover shadow body-classes="py-5">
            <div class="px-6">
              <img
                v-lazy="'img/services/service-dental.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Dental service image"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Oral and Maxillofacial Surgery, Article Implants,
                    Endodontists, Orthodontists, Periodontists.</small
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
                v-lazy="'img/services/service-surgery.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Surgery service image"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Tonsils, Appendix, Gallbladder, Kidney Stones, Uterus
                    Removal, Ovarian Cyst, Hernias.</small
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
                v-lazy="'img/services/service-specialists.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Specialists service image"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >Internal Medicine, Dermatology, Psychology, Psychiatry,
                    Pediatrics, Hematology.</small
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
                v-lazy="'img/services/service-laboratory.jpg'"
                class="rounded-square img-center img-fluid shadow shadow-lg--hover"
                style="width: 200px;"
                alt="Laboratory service image"
              />
              <div class="pt-4 text-center">
                <h5 class="title">
                  <small class="h6 text-muted"
                    >X-rays, Laboratory and Radiodiagnosis.</small
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
<script>
export default {
  name: 'Services'
}
</script>
