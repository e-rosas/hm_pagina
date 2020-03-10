<template>
  <div id="app">
    <Hero></Hero>
  </div>
</template>

<script>
import Hero from './components/Hero'
export default {
  layout: 'App',
  name: 'Index',
  components: {
    Hero
  }
}
</script>
