<!-- //A child component can accept input from the parent via props. -->
<script setup>
  const props = defineProps({
    msg: String,
  });
</script>

<template>
  <h2>{{ msg || "No props passed yet" }}</h2>
</template>
