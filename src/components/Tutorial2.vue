<script setup>
import { ref, reactive } from "vue";

// component logic
const message = ref("hello world there");
let counter = reactive({
  count: 0,
});

counter.count++;
// declare some reactive state here.
message.value = "changed";

defineProps({
  heading: String,
});

const count = ref(0);
</script>

<template>
  <hr />
  <h1>{{ heading }}</h1>
  <h1>{{ message }} {{ counter.count }}</h1>
  <h2>Tutorial step 2</h2>
  <h2>
    {{ counter.count + " " + message.split("").reverse().join("") }}
  </h2>
  <button>click me</button>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
