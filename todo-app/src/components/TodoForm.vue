<template>
    <div>
      <b-form-input v-model="newTodo" />
      <b-button @click="addTodo">Add</b-button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newTodo: ''
      }
    },
    methods: {
      addTodo() {
       
      }
    }
  }
  </script>