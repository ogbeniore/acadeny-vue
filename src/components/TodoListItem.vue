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
    },
  },
  methods: {
    deleteItem() {
      this.$emit('delete')
    }
  },
  // beforeCreate() {
  //   alert('beforeCreate')
  //   console.log('beforecreated')
  // },
  // created() {
  //   alert('created')
  //   console.log('created')
  // },
  // beforeMount() {
  //   alert('beforeMount')
  //   console.log('beforeMount')
  // },
  // mounted() {
  //   alert('Mounted')
  //   console.log('mounted')
  // },
  // beforeUpdate() {
  //   alert('beforeUpdate')
  //   console.log('beforeupdate')
  // },
  // updated() {
  //   alert('updated')
  //   console.log('updated')
  // },
  // beforeDestroy() {
  //   alert('beforeDestroy')
  //   console.log('beforeDestroy')
  // },
  // destroyed() {
  //   alert('destroyed')
  //   console.log('destroyed')
  // }
}
</script>