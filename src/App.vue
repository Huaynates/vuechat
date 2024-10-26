<template>
  <section>
    <h1 class="text-3xl font-bold underline">Mi aplicacion dee vue</h1>
    <MyCounter :value="5"></MyCounter>
    <MyCounter2 :value="5"></MyCounter2>
  </section>
</template>
<script lang="ts" setup>
import MyCounter from './components/MyCounter.vue';
import MyCounter2 from './components/my-counter/MyCounter2.vue';
</script>
