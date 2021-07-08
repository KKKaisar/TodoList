<template>
  <ul>
    <li v-for="(todo, i) in todos" @click="rmTodo(i)" :key="i + 1">
      {{ `${i + 1} ${todo}` }}
    </li>
  </ul>
</template>

<script>
export default {
  props: ["todos"],
  methods: {
    rmTodo(i) {
      this.$emit("remove-todo", i);
    },
  },
};
</script>