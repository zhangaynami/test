<template>
    <ul class="todo-main">
        <TodoItems v-for="todo in todos" :key="todo.id" :todo="todo" :checkTodo="checkTodo"></TodoItems>
    </ul>
</template>

<script>
import TodoItems from "./TodoItems.vue"
export default {
    name: "TodoList",
    components:{TodoItems},
    props:["todos","checkTodo"]

}
</script>
<style scoped>
.todo-main {
    margin-left: 0;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding: 0px;
}

.todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
}
</style>