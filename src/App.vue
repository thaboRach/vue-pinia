<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="app">
    <nav>
      <RouterLink to="/">Home</RouterLink> |
      <RouterLink to="/about">About</RouterLink>
    </nav>
    <RouterView />
  </div>
</template>

<style lang="css" scoped>
.app {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
</style>
