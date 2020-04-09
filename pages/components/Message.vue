<template>
  <section id="message" class="section section-lg pt-lg-0">
    <div class="container">
      <div class="alert alert-info" role="alert">
        <b>Hospital México and COVID-19</b>
      </div>
      <div class="row justify-content-center">
        <div class="col-lg-12">
          <div class="row row-grid align-items-center">
            <div class="col-lg-12">
              <card class="border-0" hover shadow body-classes="py-5">
                <div class="row">
                  <div class="col-md-8">
                    <h6 class="text-primary text-uppercase">
                      Hospital México remains open
                    </h6>
                    <p class="description mt-3">
                      The United States has temporarily limited inbound land
                      border crossings from Canada and México to “essential
                      travel”. This action does not prevent U.S citizens and
                      lawful permanent residents from returning to the United
                      States.
                    </p>
                    <div class="text-right">
                      <a href="https://mx.usembassy.gov/wha-press-guidance/"
                        >U.S. Embassy</a
                      >
                    </div>

                    <p class="description mt-3">
                      Hospital México is taking all the necessary precautions to
                      guarantee your safety and well-being. Please call us at
                      <a
                        href="tel:18003158714"
                        target="_blank"
                        rel="noopener"
                        data-toggle="tooltip"
                        title="Call Us"
                        >1 800 315 87 14</a
                      >
                      for any questions you may have.
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
