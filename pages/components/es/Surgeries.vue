<template>
  <section id="pricing" class="section mt--100">
    <div class="container">
      <div class="row row-grid align-items-center">
        <div class="col-md-4 order-md-1">
          <div class="pr-md-5">
            <icon
              name="fa fa-usd"
              class="mb-5"
              size="lg"
              type="success"
              shadow
              rounded
            ></icon>
            <h3>COMPARE COSTOS</h3>
            <p>Compare los costos de cirugias en E.U. y Hospital México.</p>
          </div>
        </div>
        <div class="col-md-8 order-md-2">
          <b-table
            responsive
            head-variant="light"
            hover
            :items="services"
          ></b-table>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      services: [
        {
          procedimiento: 'Cirugía de amigdalas',
          hospital_méxico: '$1,700 dlls.',
          USA: '$5,500 dlls.'
        },
        {
          procedimiento: 'Cirugía de apendice',
          hospital_méxico: '$2,300 dlls.',
          USA: '$10,000 dlls.'
        },
        {
          procedimiento: 'Cirugía de vesícula',
          hospital_méxico: '$4,300 dlls.',
          USA: '$16,000 dlls.'
        },
        {
          procedimiento: 'Cirugía de piedras en riñón',
          hospital_méxico: '$3,100 dlls.',
          USA: '$12,000 dlls.'
        }
      ]
    }
  }
}
</script>
