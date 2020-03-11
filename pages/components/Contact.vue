<template>
  <section class="section section-lg pt-0">
    <div class="container">
      <card gradient="secondary" no-body shadow-size="lg" class="border-0">
        <div class="p-5">
          <div class="row">
            <div class="col-lg-4">
              <div class="pr-md-5">
                <icon
                  name="fa fa-question-circle"
                  class="mb-5"
                  size="lg"
                  type="info"
                  shadow
                  rounded
                ></icon>
                <h2 class="">
                  Contact us
                </h2>
                <ul class="list-unstyled mt-5">
                  <li class="py-2">
                    <div class="d-flex align-items-center">
                      <a
                        class="nav-link nav-link-icon"
                        href="tel:18003158714"
                        target="_blank"
                        rel="noopener"
                        data-toggle="tooltip"
                        title="Call Us"
                      >
                        <badge
                          type="info"
                          circle
                          class="mr-3"
                          icon="fa fa-phone"
                        ></badge>
                        <h6 class="mb-0">In USA 1 800 315 87 14</h6>
                      </a>
                    </div>
                  </li>
                  <li class="py-2">
                    <a
                      class="nav-link nav-link-icon"
                      href="tel:01152(664)6836363"
                      target="_blank"
                      rel="noopener"
                      data-toggle="tooltip"
                      title="Call Us"
                    >
                      <badge
                        type="info"
                        circle
                        class="mr-3"
                        icon="fa fa-phone"
                      ></badge>
                      <h6 class="mb-0">To México 011 52 (664) 683 63 63</h6>
                    </a>
                  </li>
                  <li class="py-2">
                    <a
                      class="nav-link nav-link-icon"
                      href="mailto:info@hospitalmexico.org"
                      target="_blank"
                      rel="noopener"
                      data-toggle="tooltip"
                      title="Email Us"
                    >
                      <badge
                        type="info"
                        circle
                        class="mr-3"
                        icon="fa fa-envelope"
                      ></badge>
                      <h6 class="mb-0">info@hospitalmexico.org</h6>
                    </a>
                  </li>
                  <li class="py-2">
                    <a
                      class="nav-link nav-link-icon"
                      target="_blank"
                      rel="noopener"
                      data-toggle="tooltip"
                      title="Address"
                    >
                      <badge
                        type="info"
                        circle
                        class="mr-3"
                        icon="fa fa-map-marker"
                      ></badge>
                      <h6 class="mb-0">
                        Hospital México 9077 De la Amistad Av., Colonia Federal,
                        22010 Tijuana, B.C.
                      </h6>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col-lg-8 resp-container vue-friendly-iframe">
              <vue-friendly-iframe
                class="iframe"
                :src="maps"
              ></vue-friendly-iframe>
            </div>
          </div>
        </div>
      </card>
    </div>
  </section>
</template>
<style>
.resp-container {
  position: relative;
  overflow: hidden;
  padding-top: 56.25%;
}
.vue-friendly-iframe iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}
</style>
<script>
export default {
  data() {
    return {
      maps:
        'https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d13454.759000387881!2d-117.03046125927736!3d32.53443218857138!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x6bd2e723d983788e!2sHospital+M%C3%A9xico!5e0!3m2!1ses-419!2smx!4v1545940046180'
    }
  }
}
</script>
