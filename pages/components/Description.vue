<template>
  <section class="section">
    <div class="container">
      <div class="row row-grid align-items-center">
        <div class="col-md-6 order-md-1">
          <div class="pr-md-5">
            <icon
              name="fa fa-hospital-o"
              class="mb-5"
              size="lg"
              type="success"
              shadow
              rounded
            ></icon>
            <h1>Affordable health care for over 25 years.</h1>
            <ul class="list-unstyled mt-5">
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-clock-o"
                  ></badge>
                  <h6 class="mb-0">
                    Get immediate care and surgery at Hospital México.
                  </h6>
                </div>
              </li>
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-calendar-times-o"
                  ></badge>
                  <h6 class="mb-0">No appointment required.</h6>
                </div>
              </li>
              <li class="py-2">
                <div class="d-flex align-items-center">
                  <badge
                    type="success"
                    circle
                    class="mr-3"
                    icon="fa fa-usd"
                  ></badge>
                  <h6 class="mb-0">
                    Save up to 70% of the cost of surgeries in the US.
                  </h6>
                </div>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-md-6 order-md-2">
          <img
            v-lazy="'img/slider/HM-main-cirugias-min.jpg'"
            class="img-fluid"
            alt="Surgeries image"
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Description',
  serverCacheKey: (props) => props.item.id
}
</script>
