<template>
    <div>
        <div v-for="todo in todos" :key="todo.id">
            <TodoItem :todo="todo" v-model:completed.sync="todo.completed" v-on:del-todo="$emit('del-todo', todo.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
    name: "todo-s",
    component: { TodoItem },
    props: ["todos"],
    components: { TodoItem }
}
</script>

<style scoped>

</style>