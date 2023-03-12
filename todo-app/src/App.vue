
<template>
  <div>
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
  font-weight: 800;
  font-size: 2rem;
  margin-top: 60px;
}

</style>
