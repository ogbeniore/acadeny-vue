<template>
  <header>
    <h1>{{ pageName }}</h1>
    <h2>{{ pageSubtitle }}</h2>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  props: {
    pageName: {
      type: String,
      default: 'My header',
      required: false
    },
    pageSubtitle: String
  },
  data() {
    return {
      name: 'Gerald',
      age: 32
    }
  },
  computed: {
    now() {
      return Date.now()
    }
  }
}
</script>

<style scoped>
header {
  background: black;
  color: #ffffff;
}
</style>