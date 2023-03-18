<template>
  <div class="todo-form">
    <input type="text" id="text-input" placeholder="Enter Your Task" v-model="newTodo" />
    <input type="button" id="submit-input" value="Submit" @click="addTodo" />
  </div>
  <div>
    <ul>
      <li class="task-item" :class="{ 'task-complated': task.isCompleted }" v-for="(task, index) in allTasks"
        :key="index" :task="task" @click="completeTask(task)">{{ task.title }}<button class="btn-clear" @click="deleteTask(index)">Delete</button></li>
    </ul>
  </div>
</template>
  
<script>

export default {
  data() {
    return {
      allTasks: [],
      newTodo: ''
    }
  },
  methods: {
    addTodo() {
      this.allTasks.push({
        title: this.newTodo,
        isCompleted: false
      });
      console.log(this.allTasks);
      this.newTodo = '';
    },
    completeTask(task) {
      task.isCompleted = true
      console.log(task.isCompleted);
    },
    deleteTask(index){
      console.log("click shod",index)
      
      this.allTasks.splice(index, 1)
    }
  },
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

.task-item {
  list-style-type: none;
  background-color: aliceblue;
  color: gray;
  font-weight: 700;
  padding: 1rem;
  margin: 0.5rem auto;
  margin-right: 2.3rem;
  text-align: center;
  overflow: hidden;
}
.btn-clear{
  background-color: rgb(225, 97, 97);
  font-size: smaller;
  margin-left: 20rem;
}

.task-complated {
  background-color: rgb(136, 213, 136);
  color: black;
  text-decoration: line-through;
}
</style>