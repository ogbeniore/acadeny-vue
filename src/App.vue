<template>
  <div id="app">
    <img :src="imageUrl" :alt="hero">
    <my-header></my-header>
    <contact-form></contact-form>
    <computed></computed>
    <Login />
  </div>
</template>

<script>
import MyHeader from './components/Header.vue'
import ContactForm from './components/ContactForm.vue'
import Computed from './components/Computed.vue'
import Login from './components/Login.vue'

export default {
  name: 'app',
  components: {
    MyHeader,
    ContactForm,
    Computed,
    Login,
  },
  data(){
    return{
      imageUrl: 'http://image.blingee.com/images19/content/output/000/000/000/79b/776844392_1899848.gif',
      hero: 'Image of Girl'
    }
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
