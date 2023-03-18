<template>
  <div class="todo-form">
    <input type="text" id="text-input" placeholder="Enter Your Task" v-model="newTodo" />
    <input type="button" id="submit-input" value="Submit" @click="addTodo" />
  </div>
  <div>
    <TodoList :new-todo="newTodo"></TodoList>
  </div>
</template>
  
<script>

import TodoList from './TodoList.vue';
export default {
  components: {
    TodoList
  },
  
  data() {
    return {
      newTodo: ''
    }
  },
  methods: {
    addTodo() {
      console.log(this.newTodo);
      this.newTodo = '';
    }

  }
}
</script>
<style>
.todo-form {
  text-align: center;
  justify-content: center;
}

#text-input {
  padding: 1rem 4rem;
  border-radius: 0.2rem;
  border: solid 2px #5422f9;

}

#submit-input {
  padding: 1rem;
  border-radius: 0.2rem;
  border: solid 2px #5422f9;
}
</style>