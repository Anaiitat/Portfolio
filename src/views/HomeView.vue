<script setup>
import TheHeader  from '../components/TheHeader.vue'
import ThePresentation from '../components/ThePresentation.vue'
import TheCreation from'../components/TheCreation.vue'
import TheContact from '../components/TheContact.vue'
import TheFooter from '../components/TheFooter.vue'
</script>

<template>
  <TheHeader />
  <main>
    <h1>Portfolio</h1>
    <ThePresentation />
    <TheCreation />
    <TheContact />
    <TheFooter />
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

h2{
    font-size: 30px;
    margin: 20px;
    padding: 10px;
    font-weight: bold;
    color: rgba(112, 199, 255, 255);
    text-shadow:1px 1px 2px rgb(0, 0, 0) ;
    background-color: rgba(255, 255, 255, 0.863);
    border: 1px, solid, rgba(112, 199, 255, 255);
    border-radius: 10px;
}


</style>