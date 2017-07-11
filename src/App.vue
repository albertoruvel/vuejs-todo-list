<template>
  <div>
    <todo-list v-bind:todos="todos"></todo-list>
    <create-todo v-on:add="addTodo"></create-todo>
  </div>
</template>

<script>
import TodoList from '@/components/TodoList'
import CreateTodo from '@/components/CreateTodo'
export default {
  name: 'app',
  components: {
    TodoList,
    CreateTodo
  },
  // data function avails data to the template
  data () {
    return {
      todos: [{
        title: 'Project one',
        description: 'description one',
        done: false
      }, {
        title: 'Project two',
        description: 'description two',
        done: false
      }, {
        title: 'Project three',
        description: 'description three',
        done: true
      }, {
        title: 'Project four',
        description: 'description four',
        done: false
      }]
    }
  },
  methods: {
    addTodo (title) {
      this.todos.push({
        title,
        done: false
      })
    }
  }
}
</script>

<style>
</style>
