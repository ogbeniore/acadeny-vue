<template>
  <div id="app">
    <!-- <img src="./assets/hero-image.jpg" alt="hero"> -->
    <my-header></my-header>
    <contact-form></contact-form>
    <computed></computed>
  </div>
</template>

<script>
import MyHeader from './components/Header.vue'
import ContactForm from './components/ContactForm.vue'
import Computed from './components/Computed.vue'

export default {
  name: 'app',
  components: {
    MyHeader,
    ContactForm,
    Computed
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
