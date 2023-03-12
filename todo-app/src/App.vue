<template>
  <div>
    <!-- <br/> -->
    <p>Todo App</p>
    <TodoForm />
  </div>
</template>

<script>
import TodoForm from './components/TodoForm.vue';

export default {
  name: 'App',
  components: {
    TodoForm
  }
}
</script>

<style>
body {
  background-color: #7853f0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #b0d8ff;
  background-color: #6502bb;
  font-weight: 800;
  font-size: 2rem;
  margin-top: 60px;
  width: 40%;
  height: auto;
  margin: 0 auto;
  padding-bottom: 5rem;
}

</style>