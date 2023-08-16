<script setup>
import { ref } from "vue";

const titleClass = ref("title");

defineProps({
  heading: String,
});
</script>

<template>
  <!-- add dynamic class binding here -->
  <hr />
  <h2>{{ heading }}</h2>
  <h3 :class="titleClass">Make me red</h3>
  <p>
    Directive values are JavaScript expressions that have access to the
    component's state. The full details of v-bind and directive syntax are
    discussed in
    <a href="https://v3.vuejs.org/guide/template-syntax.html#v-bind-shorthand"
      >the Template Syntax guide</a
    >
  </p>
</template>

<style>
.title {
  color: red;
}
p {
  text-wrap: balance;
}
</style>
