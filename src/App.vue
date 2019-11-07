<template>
  <div id="app">
    <my-header
      :page-subtitle="subtitle">
    </my-header>
    <img
      :src="imageUrl"
      :alt="hero"
      :class="{'red-border': isRed}"
      class="img-fluid">
    <todo-list />
    <br>
    <br>
    <br>
    <br>
    <br>
    
    <MyHeader
      v-for="header in myHeaders"
      :key="header.id"
      :page-name="header.name"
      :page-subtitle="header.subtitle"  
    />
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
      imageUrl: 'http://image.blingee.com/images19/content/output/000/000/000/79b/776844392_1899848.gif',
      hero: 'Image of Girl',
      imgClass: 'red-border',
      isRed: true,
      name: 'My Todo App',
      subtitle: 'Hello world',
      myHeaders: [
        {
          id: 1,
          name: 'Headr 1',
          subtitle: 'sub 1'
        },
        {
          id: 2,
          name: 'Headr 2',
          subtitle: 'sub 2'
        },
        {
          id: 3,
          name: 'Headr 3',
          subtitle: 'sub 3'
        },
        {
          id: 4,
          name: 'Headr 4',
          subtitle: 'sub 4'
        },
      ]
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
.red-border {
  border: 2px solid red;
}
.img-fluid {
  width: 100%;
  height: auto;
}
</style>
