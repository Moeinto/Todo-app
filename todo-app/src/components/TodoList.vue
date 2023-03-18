<template>
    <ul>
        <li v-for="(task, index) in allTasks" :key="index" :task="task" @completed="completeTask">{{ task.title }}</li>

    </ul>
</template>

<script>
export default {

    data() {
        return {
            allTasks: [],
        }
    }s
    ,
    methods: {
        addTodo() {
            this.allTasks.push({
                title: this.newTodo,
                isCompleted: false
            })
            console.log(this.allTasks)
            this.newTodo = ''
        },
        completeTask(task) {
            task.isCompleted = true;
        }
    },
}
</script>

<style></style>