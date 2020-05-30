<template>
  <ul class="todo-list">
    <todo-item v-for="item of list" :key="item.id" :todo="item" />
  </ul>
</template>

<script>
import TodoItem from './TodoItem'
export default {
  name: 'TodoList',
  components: { TodoItem },
  props: {
    list: {
      type: Array,
      required: false,
      default: () => ([])
    }
  }
}
</script>

<style scoped lang="sass">
.todo-list
  list-style: none
</style>
