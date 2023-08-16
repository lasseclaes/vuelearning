<script setup>
import { ref } from "vue";
import ChildComp from "./Tutorial14slots.vue";

const msg = ref("from parent");

defineProps({
  heading: String,
});
</script>

<template>
  <hr />
  <h2>{{ heading }}</h2>
  <ChildComp>My message: {{ msg }} </ChildComp>
</template>
