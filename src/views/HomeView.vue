<script setup>
import TheHeader  from '../components/TheHeader.vue'
import ThePresentation from '../components/ThePresentation.vue'
</script>

<template>
  <TheHeader />
  <main>
    <h1>Portfolio</h1>
    <ThePresentation />
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

#presentation,
#creation,
#contact{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: rgba(114, 161, 192, 0.459);
    border-radius: 20px;
}


</style>