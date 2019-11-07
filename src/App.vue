<template>
  <div id="app">
    <my-header :pageName="name">
      <table>
        <thead>
          <tr>
            <th>rrrr</th>
            <th>tttt</th>
            <th>ttyttt</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>rhbffhb</td>
            <td>rkjbnkjhb</td>
            <td>rjkbkjbnf</td>
          </tr>
          <tr>
            <td>rhbffhb</td>
            <td>rkjbnkjhb</td>
            <td>rjkbkjbnf</td>
          </tr>
          <tr>
            <td>rhbffhb</td>
            <td>rkjbnkjhb</td>
            <td>rjkbkjbnf</td>
          </tr>
          <tr>
            <td>rhbffhb</td>
            <td>rkjbnkjhb</td>
            <td>rjkbkjbnf</td>
          </tr>
          <tr>
            <td>rhbffhb</td>
            <td>rkjbnkjhb</td>
            <td>rjkbkjbnf</td>
          </tr>
          <tr>
            <td>rhbffhb</td>
            <td>rkjbnkjhb</td>
            <td>rjkbkjbnf</td>
          </tr>
        </tbody>
      </table>
    </my-header>
    <my-header pageName="jdjdjj">
      <template v-slot:ore>
        <label for="lol">Lolo</label>
        <input type="text" name="" id="">
      </template>
      <template v-slot:bottom> 
        <table>
          <thead>
            <tr>
              <th>rrrr</th>
              <th>tttt</th>
              <th>ttyttt</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>rhbffhb</td>
              <td>rkjbnkjhb</td>
              <td>rjkbkjbnf</td>
            </tr>
            <tr>
              <td>rhbffhb</td>
              <td>rkjbnkjhb</td>
              <td>rjkbkjbnf</td>
            </tr>
            <tr>
              <td>rhbffhb</td>
              <td>rkjbnkjhb</td>
              <td>rjkbkjbnf</td>
            </tr>
            <tr>
              <td>rhbffhb</td>
              <td>rkjbnkjhb</td>
              <td>rjkbkjbnf</td>
            </tr>
            <tr>
              <td>rhbffhb</td>
              <td>rkjbnkjhb</td>
              <td>rjkbkjbnf</td>
            </tr>
            <tr>
              <td>rhbffhb</td>
              <td>rkjbnkjhb</td>
              <td>rjkbkjbnf</td>
            </tr>
          </tbody>
        </table>
      </template>
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
