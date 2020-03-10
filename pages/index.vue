<template>
  <div id="app">
    <MainSlider></MainSlider>
    <Description></Description>
    <Services></Services>
    <Surgeries></Surgeries>
    <Insurances></Insurances>
  </div>
</template>

<script>
import MainSlider from './components/MainSlider'
import Description from './components/Description'
import Services from './components/Services'
import Surgeries from './components/Surgeries'
import Insurances from './components/Insurances'
export default {
  layout: 'App',
  name: 'Index',
  components: {
    MainSlider,
    Description,
    Services,
    Surgeries,
    Insurances
  }
}
</script>
