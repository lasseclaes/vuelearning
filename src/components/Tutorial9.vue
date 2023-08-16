<script setup>
import { ref, onMounted } from "vue";
const pElementRef = ref(null);

onMounted(() => (pElementRef.value.textContent = "hey"));

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <p ref="pElementRef">hello</p>
</template>
