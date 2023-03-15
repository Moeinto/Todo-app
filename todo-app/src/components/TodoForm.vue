<template>
  <div class="todo-form">
    <input type="text" id="text-input" placeholder="Enter Your Task" v-model="newTodo" />
    <input type="button" id="submit-input" value="Submit" @click="addTodo" />
  </div>
  <div>
    <ul>
      <li v-for="(task, index) in allTasks" :key="index" :task="task" @completed="completeTask">{{ task.title }}</li>
    </ul>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      newTodo: '',
      allTasks: []
    }
  },
  methods: {
    addTodo() {
      this.allTasks.push({
        title: this.newTodo,
        isComplated : false
      })
      console.log(this.allTasks)
      this.newTodo = ''
    },
    completeTask(task) {
      task.isCompleted = true;
    }

  }
}
</script>
<style>
.todo-form{
  text-align: center;
  justify-content: center;
}
#text-input{
  padding: 1rem 4rem;
  border-radius: 0.2rem;
  border: solid 2px #5422f9;
  
}
#submit-input{
  padding: 1rem;
  border-radius: 0.2rem;
  border: solid 2px #5422f9;
}
</style>