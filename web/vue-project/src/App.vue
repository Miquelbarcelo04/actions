<template>
  <div class="keypad">
    <button v-for="number in numbers" :key="number" @click="handleClick(number)">
      {{ number }}
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const numbers = ref([1, 2, 3, 4, 5, 6, 7, 8, 9]);

const handleClick = (number) => {
  alert(`Has clicat el número ${number}`);
};
</script>

<style scoped>
.keypad {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
}

.keypad button {
  width: 2rem;
  height: 2rem;
  font-size: 1.5rem;
}
</style>
