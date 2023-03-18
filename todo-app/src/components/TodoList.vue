<template>
    <ul>
        <li v-for="(task, index) in allTasks" :key="index" :task="task">{{ task.title }}</li>
    </ul>
</template>

<script>
export default {
    props : {
    allTasks : Object
    }
    ,
    data() {
        return {
         
        }
    }
    ,
    methods: {
       
    },
}
</script>

<style></style>