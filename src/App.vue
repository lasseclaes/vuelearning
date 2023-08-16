<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import Tutorial2 from "./components/Tutorial2.vue";
import Tutorial3 from "./components/Tutorial3.vue";
import Tutorial4 from "./components/Tutorial4.vue";
import Tutorial5 from "./components/Tutorial5.vue";
import Tutorial6 from "./components/Tutorial6.vue";
import Tutorial7 from "./components/Tutorial7.vue";
import Tutorial8 from "./components/Tutorial8.vue";
import Tutorial9 from "./components/Tutorial9.vue";
import Tutorial10 from "./components/Tutorial10.vue";
import Tutorial11 from "./components/Tutorial11.vue";
import Tutorial12 from "./components/Tutorial12.vue";
import Tutorial13 from "./components/Tutorial13.vue";
import Tutorial14 from "./components/Tutorial14.vue";
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
  <Tutorial2 heading="Learnings from tutorails" />
  <Tutorial3 heading="Tutorial step 3" />
  <hr />
  <Tutorial4 heading="Tutorial step 4" />
  <Tutorial5 heading="Tutorial step 5" />
  <Tutorial6 heading="Tutorial step 6" />
  <Tutorial7 heading="Tutorial step 7" />
  <Tutorial8 heading="Tutorial step 8" />
  <Tutorial9 heading="Tutorial step 9: On Mounted" />
  <Tutorial10 heading="Tutorial step 10: fetch and side effects" />
  <Tutorial11 heading="Tutorial step 11: components" />
  <Tutorial12 heading="Tutorial step 12: components & props" />
  <Tutorial13 heading="Tutorial step 13: child emits props up hierarchy" />
  <Tutorial14 heading="Tutorial step 14: slots" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
