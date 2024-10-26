<template>
  <section>
    <h3>Counter {{ counter }}</h3>
    <h3>Square {{ squareCounter }}</h3>
    <div>
      <button class="btn" @click="counter++">+1</button>
      <button class="btn" @click="counter--">-1</button>
    </div>
  </section>
</template>
<script lang="ts" setup>
import { useCounter } from './composables/useCounter';
interface props {
  value?: number;
}
const props = defineProps<props>();

const { counter, squareCounter } = useCounter(props.value);
/*
import { computed, ref } from 'vue';
/*
const props = defineProps({
  value: { type: Number, required: false },
});
/

interface props {
  value?: Number;
}
const props = defineProps<props>();
const counter = ref(props.value ?? 5);
const squareCounter = computed(() => counter.value * counter.value);
*/
</script>
<style>
.btn {
  @apply p-5 bg-blue-500 rounded mr-2 hover:bg-blue-700;
}
</style>
