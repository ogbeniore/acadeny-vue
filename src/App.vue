<template>
  <div id="app">
    <my-header :pageName="name">
    </my-header>
    <todo-list />
  </div>
</template>

<script>
import MyHeader from './components/Header.vue'
import TodoList from './components/TodoList.vue'

export default {
  name: 'app',
  components: {
    MyHeader,
    TodoList
  },
  data(){
    return{
      name: 'My Todo App',
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
