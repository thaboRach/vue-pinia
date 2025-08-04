<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';

const storeCounter = useCounterStore();
</script>

<template>
  <p class="count">{{ storeCounter.count }}</p>
</template>
