<template>
    <ul>
        <li v-for="(task, index) in tasks" :key="index" :task="task" @task-completed="completeTask"></li>
    </ul>
</template>
<script>
export default {
    data(){
        return{
            tasks : [],
        }
    },methods: {
        
    },



}

</script>
<style></style>