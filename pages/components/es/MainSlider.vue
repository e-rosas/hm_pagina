<template>
  <div>
    <b-carousel id="carousel-2" :interval="4000" controls indicators>
      <!-- Text slides with image -->
      <b-carousel-slide
        img-src="/img/slider/main/HM-main-fachada.jpg"
        img-fluid
        style="max-height:450px;"
        img-alt="HM Fachada"
      >
        <h2 style="color: white;">Hospital México está abierto</h2>
        <div class="row d-none d-md-block">
          <h3 style="color: white;">
            Está bien venir a México por tratamiento médico
          </h3>
          <h5 style="color: white;">
            Por favor llámenos al
            <a
              href="tel:18003158714"
              style="color: blue;"
              target="_blank"
              rel="noopener"
              data-toggle="tooltip"
              title="Llámenos"
              >1 800 315 87 14</a
            >
            o al
            <a
              href="tel:18003158714"
              style="color: blue;"
              target="_blank"
              rel="noopener"
              data-toggle="tooltip"
              title="Llámenos"
              >011 52 664 683 6363 </a
            >para cualquier duda o pregunta.
          </h5>
        </div>
      </b-carousel-slide>
      <!-- <b-carousel-slide
        img-src="/img/slider/main/HM-main-fachada.jpg"
        style="height:450px;"
      >
        <h1 style="color: white;">Abierto 24 horas, de lunes a domingo.</h1>
      </b-carousel-slide> -->

      <b-carousel-slide
        caption=""
        text="No se requiere cita."
        img-src="/img/slider/main/HM-main-resultados.jpg"
        img-fluid
        style="max-height:450px;"
        img-alt="HM Resultados"
      >
        <h3 style="color: white;">Cosulta y resultados el mismo día.</h3>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>
<script>
export default {
  name: 'Slider'
}
</script>
