<template>
  <div id="app">
    <TodoList :todos="todos" @remove-todo="removeTodo" />
  </div>
</template>

<script>
import TodoList from "@/components/TodoList";

export default {
  name: "App",
  data() {
    return {
      todos: ["First", "Second"],
    };
  },
  components: { TodoList },
  methods: {
    removeTodo(i) {
      this.todos.splice(i, 1);
    },
  },
};
</script>

<style>
</style>
