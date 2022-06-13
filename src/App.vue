<script lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style>
@import '@/assets/base.css';

#app {
  height: 100vh;
  background-image: url("/src/assets/images/background.png");
  background-size: cover;
  background-position: center;
  padding: 2rem;
  font-weight: normal;

  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
