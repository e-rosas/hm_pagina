<template>
  <div>
    <b-carousel
      id="carousel-1"
      :interval="4000"
      controls
      indicators
      img-width="1400"
      img-height="300"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        text="Surgeries and Hospitalization."
        img-src="http://hospitalmexico.org/images/slider/HM-main-fachada.jpg"
      >
        <h1 style="color: white;">Open 24 hours, Monday through Sunday.</h1>
      </b-carousel-slide>

      <b-carousel-slide
        caption=""
        text="No appointment needed."
        img-src="http://hospitalmexico.org/images/slider/HM-main-resultados.jpg"
      >
        <h1 style="color: white;">Same day consultation and results.</h1>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>
<script>
export default {}
</script>
