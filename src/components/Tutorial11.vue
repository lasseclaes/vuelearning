<script setup>
import { ref } from "vue";
import ChildComp from "./Tutorial11child.vue";

defineProps({
  heading: String,
});
</script>

<template>
  <!-- render child component -->
  <hr />
  <h2>{{ heading }}</h2>
  <ChildComp />
</template>
