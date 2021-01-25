<template>
  <div id="app">
    <MainSlider></MainSlider>
    <Message></Message>
    <Description></Description>
    <Services></Services>
    <Surgeries></Surgeries>
    <Insurances></Insurances>
    <Tourism></Tourism>
    <Contact></Contact>
  </div>
</template>

<script>
import MainSlider from '../components/es/MainSlider'
import Description from '../components/es/Description'
import Services from '../components/es/Services'
import Surgeries from '../components/es/Surgeries'
import Insurances from '../components/es/Insurances'
import Contact from '../components/es/Contact'
import Tourism from '../components/es/Tourism'
import Message from '../components/es/Message'
export default {
  layout: 'AppEs',
  name: 'IndexEsp',
  components: {
    MainSlider,
    Description,
    Services,
    Surgeries,
    Insurances,
    Contact,
    Tourism,
    Message
  },
  data() {
    return {
      title: 'Hospital Mexico​ en Tijuana',
      description:
        'Hospital Mexico en Tijuana ha brindado atencion medica por mas de 25 años. Llame ahora en caso de tener alguna duda o pregunta.'
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
          hid: 'description',
          name: 'description',
          content: this.description
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content:
            'Hospital, Tijuana, México,​ Dental,Cirugias accesibles, San Diego, Linea, Citas, Mexico, Accesible'
        }
      ]
    }
  }
}
</script>
