<template>
  <div id="app">
    <Hero/>

    <Properties/>


    <Footer/>
  </div>
</template>

<script>

import Hero from './components/Hero.vue'
import Footer from './components/Footer.vue'
import Properties from './components/Properties.vue'

export default {
  name: 'app',
  components: {
      Hero,
      Footer,
      Properties
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
}
</style>
