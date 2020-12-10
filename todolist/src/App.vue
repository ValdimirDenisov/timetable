<template>
  <div id="app">
    <TodoList v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './components/todolist.vue'

export default {
  name: 'app',
  data(){
    return {
      todos: ['Зарядка', 'Завтрак', 'Проснуться', 'почистить зубы']
    }
  },
  components: {
    TodoList
  },
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>
  body {
    background-color: #a1e300;
  }
  #app {
    width: 450px;
    height: 350px;
    margin: auto;
    margin-top: 120px;
    background-color: rgb(70, 86, 230);
    padding: 40px;
    border-radius: 15px;
  }
</style>