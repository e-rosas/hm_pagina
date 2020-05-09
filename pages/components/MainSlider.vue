<template>
  <div>
    <b-carousel id="carousel-1" :interval="4000" controls indicators>
      <!-- Text slides with image -->
      <b-carousel-slide
        img-src="/img/slider/main/HM-main-fachada.jpg"
        img-fluid
        style="max-height:450px;"
        img-alt="HM fachada"
      >
        <h2 style="color: white;">Hospital México remains open</h2>
        <div class="row d-none d-md-block">
          <div class="col-lg-12">
            <h3 style="color: white;">
              It is okay to come to México for medical treatment
            </h3>
            <h4 style="color: white;">
              Please call us at
              <a
                href="tel:18003158714"
                style="color: blue;"
                target="_blank"
                rel="noopener"
                data-toggle="tooltip"
                title="Call Us"
                >1 800 315 87 14</a
              >
              or
              <a
                href="tel:18003158714"
                style="color: blue;"
                target="_blank"
                rel="noopener"
                data-toggle="tooltip"
                title="Call Us"
                >011 52 664 683 6363 </a
              >for any questions.
            </h4>
          </div>
        </div>
      </b-carousel-slide>
      <!-- <b-carousel-slide
        text="Surgeries and Hospitalization."
        img-src="img/slider/main/HM-main-fachada.jpg"
        style="height:450px;"
      >
        <h1 style="color: white;">Open 24 hours, Monday through Sunday.</h1>
      </b-carousel-slide> -->

      <b-carousel-slide
        caption=""
        text="No appointment needed."
        img-src="img/slider/main/HM-main-resultados.jpg"
        img-fluid
        style="max-height:450px;"
        img-alt="HM results"
      >
        <h2 style="color: white;">Same day consultation and results.</h2>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>
<script>
export default {
  name: 'MainSlider'
}
</script>
