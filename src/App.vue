<template>
  <div id="app">
    <h1>Todo List</h1>
    <h3>Completed:{{completedTodos}}</h3>
    <h3>Pending:{{pendingTodoCount}}</h3>
    <todo-list/>
     <todo-form/>
  </div>
</template>

<script>
import {mapGetters} from "vuex";
import TodoList from './components/TodoList';
import TodoForm from './components/TodoForm';

export default {
  name: 'App',
  components: {
    TodoList,
    TodoForm
  },
  computed:{
    ...mapGetters({

        completedTodos:'completedTodos',
        pendingTodoCount:'pendingTodos'
    })
    // completedTodos(){
    //   return this.$store.getters.completedTodos
    // },
    // pendingTodoCount(){
    //   return this.$store.getters.pendingTodos

    // }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
