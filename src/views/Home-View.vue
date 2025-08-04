<script setup lang="ts">
import Counter from '@/components/Counter.vue';
import { useCounterStore } from '@/stores/counter';

const storeCounter = useCounterStore();
</script>

<template>
  <div class="home">
    <Counter />
    <div class="buttons">
      <button type="button" @click="storeCounter.decreaseCount">-</button>
      <button type="button" @click="storeCounter.increaseCount">+</button>
    </div>
    <hr />
    <p>This counter is: {{ storeCounter.oddOrEven }}</p>
    <hr />
    <div>
      <h3>Edit counter:</h3>
      <input v-model="storeCounter.count" type="number" />
    </div>
  </div>
</template>

<style lang="css" scoped>
.home {
  display: flex;
  flex-direction: column;
}

.count {
  font-size: 60px;
  margin: 20px;
}

.buttons {
  display: flex;
  justify-content: space-between;
}

h3 {
  font-weight: 700;
  font-size: 26px;
}
</style>
