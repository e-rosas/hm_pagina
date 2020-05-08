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
import MainSlider from './components/MainSlider'
import Description from './components/Description'
import Services from './components/Services'
import Surgeries from './components/Surgeries'
import Insurances from './components/Insurances'
import Contact from './components/Contact'
import Tourism from './components/Tourism'
import Message from './components/Message'
export default {
  layout: 'App',
  name: 'Index',
  serverCacheKey: (props) => props.item.id,
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
      title: 'Hospital México​ in Tijuana, providing affordable health care.',
      description:
        'Hospital Mexico in Tijuana has been providing affordable health care for over 25 years. Call now for any questions you may have.'
    }
  },
  head() {
    return {
      title: this.title,
      htmlAttrs: {
        lang: 'en'
      },
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Hospital México​ in Tijuana',
          name: 'Hospital México​ in Tijuana',
          description: this.description,
          content:
            'Hospital, Tijuana, México,​ Dental, Affordable surgeries, Treatments, Arthritis, Lupus, Lyme Disease, Migraine, Fibromyalgia, Mexico'
        }
      ]
    }
  }
}
</script>
