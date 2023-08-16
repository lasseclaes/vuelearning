<script setup>
import { ref } from "vue";
import ChildComp from "./Tutorial12childCompProps.vue";

const greeting = ref("Hello from parent");

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <ChildComp :msg="greeting" />
</template>
