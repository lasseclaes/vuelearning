<script setup>
import { ref, computed } from "vue";

let id = 0;

const newTodo = ref("");
const hideCompleted = ref(false);
const todos = ref([
  { id: id++, text: "Learn HTML", done: false },
  { id: id++, text: "Learn JavaScript", done: false },
  { id: id++, text: "Learn Vue", done: false },
]);

const filteredTodos = computed(() => {
  // return filtered todos based on
  // `todos.value` & `hideCompleted.value`

  // hvis komplette er skjulte ? filterer
  //   console.log("todos.value: " + todos.value);
  console.group("1. list before running filteredTodos");
  console.table(filteredTodos.value);

  let tableData = todos.value.filter((t) => !t.done);
  console.log(
    "2. filtered: Checks if done value is falsy. It filters out the items where done is true, and keeps the those not maked as done"
  );
  console.table(tableData);
  console.groupEnd();

  return hideCompleted.value ? todos.value.filter((t) => !t.done) : todos.value;
});

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value, done: false });
  newTodo.value = "";
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo);
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
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done" />
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
  <button @click="hideCompleted = !hideCompleted">
    {{ hideCompleted ? "Show all" : "Hide completed" }}
    {{ console.log("hideCompleted: " + hideCompleted) }}
  </button>
</template>

<style>
.done {
  text-decoration: line-through;
}
</style>
