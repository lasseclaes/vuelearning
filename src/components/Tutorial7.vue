<script setup>
import { ref } from "vue";

// give each todo a unique id
let id = 0;

const newTodo = ref("");
const todos = ref([
  { id: id++, text: "Learn HTML" },
  { id: id++, text: "Learn JavaScript" },
  { id: id++, text: "Learn Vue" },
]);

function addTodo() {
  // ...write code
  todos.value.push({ id: id++, text: newTodo.value });
  newTodo.value = "";
}

function removeTodo(todo) {
  // ...write code
  todos.value = todos.value.filter((t) => t.id !== todo.id);
}

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo" />
    <button>Add Todo</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>

<style>
ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  align-items: start;
}
</style>
