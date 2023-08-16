<script setup>
import { ref, watch } from "vue";

const todoId = ref(1);
const todoData = ref(null);

async function fetchData() {
  todoData.value = null;
  const res = await fetch(
    `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  );
  todoData.value = await res.json();
}

fetchData();
watch(todoId, fetchData);

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <p>Todo id: {{ todoId }}</p>
  <button @click="todoId++">Fetch next todo</button>
  <p v-if="!todoData">Loading...</p>
  <p v-else>
    {{ todoData.userId }} {{ todoData.id }} {{ todoData.title }} {{ todoData }}
  </p>
  <!-- <pre v-else>{{ todoData }}</pre> -->
</template>
