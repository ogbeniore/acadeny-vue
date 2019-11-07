<template>
  <li>
    {{todoItem}}
    <button @click="deleteItem">delete</button>
  </li>
</template>
<script>
export default {
  name: 'TodoListItem',
  props: {
    todoItem: {
      type: String,
      required: true
    }
  },
  methods: {
    deleteItem() {
      this.$emit('delete')
    }
  }
}
</script>