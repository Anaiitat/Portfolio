<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
    <div>
        <img src="../assets/404-error.png">
        <p>La page que vous cherchez semble introuvable</p>
        <RouterLink to="/" class="retour">Retour</RouterLink>
    </div>
</template>

<style scoped>
div{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    height: auto;
    background-image: url(../assets/background.png);
    background-size: cover;
    padding: 60px;
}

img{
    width: 500px;
}

p{
  border-radius: 20px;
  color:rgb(255, 255, 255);
  text-shadow:1px 1px 2px black ;
  font-size: 23px;
  margin: 20px;
}

.retour{
    border: 2px solid rgba(112, 199, 255, 1);
  background-color: rgba(112, 199, 255, 0.63);
  border-radius: 40px;
  width: 170px;
  font-weight: bold;
  color: white;
  font-size: 25px;
  text-align: center;
}

  .retour:hover{
    transition: transform 0.2s;
  transform: scale(1.1);
  }
</style>