<script setup>
import TheHeader  from '../components/TheHeader.vue'
</script>

<template>
  <TheHeader />
  <main>
    <h1>Portfolio</h1>

  </main>
  
</template>

<style scoped>
main{
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 2000px;
  background-image: url(../assets/background.png);
  background-size: cover;
}
</style>