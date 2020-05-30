<template>
  <li class="todo-item">
    <span class="todo-status" :class="{ done: todo.done, 'not-done': !todo.done }" />
    <strong class="todo-title">{{ todo.title }}</strong>
  </li>
</template>

<script>
export default {
  name: 'TodoItem',
  props: {
    todo: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped lang="sass">
.todo-item
    display: flex
    align-items: center
.todo-title
    margin-left: 10px
.todo-status
    display: inline-block
    width: 10px
    height: 10px
    border-radius: 50%
    &.done
        background: green
    &.not-done
        background: red
</style>
