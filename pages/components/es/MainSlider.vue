<template>
  <div>
    <b-carousel id="carousel-1" :interval="4000" controls indicators>
      <!-- Text slides with image -->
      <b-carousel-slide
        img-src="/img/slider/main/HM-main-fachada.jpg"
        style="height:450px;"
      >
        <h1 style="color: white;">Abierto 24 horas, de lunes a domingo.</h1>
      </b-carousel-slide>

      <b-carousel-slide
        caption=""
        text="No se requiere cita."
        img-src="/img/slider/main/HM-main-resultados.jpg"
        style="height:450px;"
      >
        <h1 style="color: white;">Cosulta y resultados el mismo día.</h1>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>
<script>
export default {}
</script>
