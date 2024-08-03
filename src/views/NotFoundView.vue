<script setup>
import { RouterLink } from "vue-router";
 
</script>


<template>
  <div class="error">
    <img src="../assets/Error404.png" alt="" class="img_error">
    <p>La page que vous recherchez semble introuvable</p>
    <RouterLink to="/" class="retour">Retour</RouterLink>
    
  </div>
</template>

<style>

.error{
  display: flex;
  flex-direction: column;
  margin: 0%;
  align-items: center;
  width: 100%;
  background-image: url(../assets/particle-lines-futuristic-gradient-background.jpg);
  background-size: cover;
}

.img_error{
  width: 700px;
}

.error > p{
  display: flex;
  flex-direction: column;
  align-items: center;
  
  border-radius: 20px;
  text-align: center;
  
  color:rgb(255, 255, 255);
  text-shadow:1px 1px 2px black ;
  font-size: 23px;
}

.retour{
  border: 2px solid rgba(112, 199, 255, 255);
  background-color: rgba(112, 199, 255, 0.63);
  border-radius: 40px;
  width: 200px;
  text-align: center;
  font-weight: bold;
  margin-top: 10px;
  color: white;
  margin: 65px;
  font-size: 25px;}

  .retour:hover{
    transition: transform 0.2s;
  transform: scale(1.1);
  }
</style>
