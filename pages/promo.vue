<template>
  <div class="container">
    <FormPromo></FormPromo>
  </div>
</template>

<script>
import FormPromo from './components/promo/FormPromo'

export default {
  layout: 'SimpleLayout',
  name: 'Promo',
  components: { FormPromo },
  data() {
    return {
      title: 'Hospital México​ - Promo',
      description: 'Register now to receive exclusive benefits'
    }
  },
  head() {
    return {
      title: this.title,

      htmlAttrs: {
        lang: 'es'
      },
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Promo',
          name: 'Promociones, Promotions, Hospital México​ Tijuana',
          content: 'Promo, Oferta, Hospital, México​, Tijuana'
        }
      ]
    }
  }
}
</script>
