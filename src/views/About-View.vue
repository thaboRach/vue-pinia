<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';

const storeCounter = useCounterStore();
</script>

<template>
  <div class="about">
    <h1>About</h1>
    <button @click="storeCounter.increaseCount" type="button" class="counter-button">
      {{ storeCounter.count }}
    </button>
  </div>
</template>

<style lang="css" scoped>
.counter-button {
  font-size: 50px;
}
</style>
