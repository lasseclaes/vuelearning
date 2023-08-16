<script setup>
import { ref } from "vue";
import ChildComp from "./Tutorial13childEmits.vue";

const childMsg = ref("No child msg yet");

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <ChildComp @response="(msg) => (childMsg = msg)" />
  <p>{{ childMsg }}</p>
</template>
