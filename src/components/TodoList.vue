<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" name="todo" class="form__item" v-model="newTodo">
      <button type="submit">Add to list</button>
    </form>
    <h1>Total items: {{ total }}</h1>
    <h1>Deleted items: {{ deletedItems }}</h1>
    <ul>
      <li v-for="(todo, index) in list" :key="index">
        {{todo}}
        <button @click="deleteItem(index)">delete</button>
      </li>
    </ul>
    <header>
      <h1>Welcome to my World</h1>
      <p>Hello, I'm oreoluwa, I am a frontend develope</p>
    </header>
    <section>
      <h2>About Me</h2>
      <p>blah blah blas</p>
    </section>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  data() {
    return {
      newTodo: '',
      list: [],
      deletedItems: 0
    }
  },
  methods: {
    addTodo() {
      this.list.push(this.newTodo)
      this.newTodo = ''
    },
    deleteItem(index) {
      this.list.splice(index, 1)
      this.deletedItems = this.deletedItems + 1 
    }
  },
  computed: {
    total() {
      return this.list.length
    }
  }
}
</script>

<style>
header {
  background: pink;
  color: black;
  padding: 10px 10px;
  border:  1px dotted pink;
}

</style>