<script setup>
import { ref } from "vue";
const text = ref("");

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <input v-model="text" placeholder="Type here" />
  <p>{{ text }}</p>
</template>
