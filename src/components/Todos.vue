<template>
    <div>
        <div v-for="todo in todos" v-bind:key="todo.id">
            <TodoItem v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)"/>
        </div>
    </div>
</template>


<script>
    import TodoItem from "./TodoItem";

    export default {
        name: "Todos",
        components: {
            TodoItem
        },
        props: ["todos"]
    }
</script>
