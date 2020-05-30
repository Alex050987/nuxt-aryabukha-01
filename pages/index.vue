<template>
  <div class="container">
    <todo-list :list="todoList" />
    <p v-show="isHidden">
      {{ text }}
    </p>
    <ul>
      <li v-for="name of names" :key="name">
        {{ name }}
      </li>
    </ul>
    <!-- <div>
      <template v-for="user of users">
        <span :key="user.email">{{ user.name }}</span> - <span :key="user.email">{{ user.email }}</span>
        <hr :key="user.email">
      </template>
    </div> -->
  </div>
</template>

<script>
import TodoList from '../components/TodoList'
export default {
  components: { TodoList },
  data: () => ({
    isHidden: false,
    text: 'I\'m visible',
    names: ['Nick', 'Eugene', 'Alex'],
    todoList: [
      {
        id: 1,
        title: 'todo 1',
        done: true
      },
      {
        id: 2,
        title: 'todo 2',
        done: false
      },
      {
        id: 3,
        title: 'todo 3',
        done: false
      }
    ],
    users: [
      {
        name: 'Nick',
        email: 'nick@gmail.com'
      },
      {
        name: 'Eugene',
        email: 'eugene@gmail.com'
      },
      {
        name: 'Alex',
        email: 'alex@gmail.com'
      }
    ]
  })
}
</script>
