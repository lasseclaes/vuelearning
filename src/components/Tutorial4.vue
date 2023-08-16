<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}

defineProps({
  heading: String,
});
</script>

<template>
  <!-- make this button work -->
  <h2>{{ heading }}</h2>
  <button @click="increment">count is: {{ count }}</button>
</template>
