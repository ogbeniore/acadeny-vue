<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" name="todo" class="form__item" v-model="newTodo">
      <button type="submit">Add to list</button>
    </form>
    <h1>Total items: {{ total }}</h1>
    <h1>Deleted items: {{ deletedItems }}</h1>
    <ul>
      <todo-list-item
        v-for="(todo, index) in list"
        :key="index"
        :todo-item="todo"
        @delete="deleteItem(index)"
        />
    </ul>
  </div>
</template>

<script>
import TodoListItem from './TodoListItem.vue'

export default {
  name: 'TodoList',
  components: {
    TodoListItem
  },
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