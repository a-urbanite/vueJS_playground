<template>
  <SimpleStateTest/>
  <!-- <ToDo></ToDo> -->
  <h1>To-Do List</h1>
  <ul>
    <li v-for="item in ToDoItems" :key="item.label">
      <ToDoItem :label="item.label" :done="item.done"></ToDoItem>
    </li>
  </ul>
</template>

<script>
import SimpleStateTest from './components/simpleStateTest.vue';
// import ToDo from './components/ToDo.vue'
import ToDoItem from './components/toDoItem.vue';
// import uniqueId from 'lodash.uniqueid';

export default {
  name: 'App',
  components: {
    SimpleStateTest,
    // ToDo,
    ToDoItem
  },
  data() {
    return {
      ToDoItems: [
        { label: 'Learn Vue', done: false },
        { label: 'Create a Vue project with the CLI', done: true },
        { label: 'Have fun', done: true },
        { label: 'Create a to-do list', done: false }
      ]
    };
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
