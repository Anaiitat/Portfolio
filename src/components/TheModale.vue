<script setup>
const props = defineProps({
  reveleModal: Boolean,
  oneCreation: Object,
});
</script>

<template>
  <div class="bloc-modale" v-if="reveleModal">
    <div class="overlay" v-on:click="toggleModale">
      <div class="modale">
        <button v-on:click="toggleModale" class="btn-modale btn btn-danger">
          X
        </button>
        <h1>{{ oneCreation.name }}</h1>
        <img :src="`./src/assets/${oneCreation.image}.png`" />
        <ul>
          <li>{{ oneCreation.date }}</li>
          <li>{{ oneCreation.technologies }}</li>
          <li class="barre"></li>
          <li>{{oneCreation.description}}</li>
          <li class="barre"></li>
          <li> <a :href="'{oneCreation.link}'">{{ oneCreation.link }}</a> </li>
          <li><a :href="'{oneCreation.link}'">{{ oneCreation.link2 }}</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: bold;
  margin: 10px;
  font-size: 40px;
  color: rgb(255, 255, 255);
  text-shadow: 1px 1px 2px black;
  border: 1px, solid, rgba(112, 199, 255, 255);
  padding: 5px 10px 10px 10px;
  background: linear-gradient(rgba(112, 199, 255, 255), pink);
  border-radius: 15px 50px 30px;
  writing-mode: vertical-rl;
  text-align: center;
}

.bloc-modale {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9998;
}

.overlay {
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
}

.modale {
  background: #f1f1f1;
  color: #333;
  padding: 20px;
  margin: 30px;
  overflow: auto;
  display: flex;
  width: 1000px;
  border-radius: 20px;
}
.btn-modale {
  position: absolute;
  top: 10px;
  right: 10px;
}

ul {
  list-style-type: none;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  
}

.barre {
  height: 3px;
  width: 200px;
  background: linear-gradient(to right,rgba(112, 199, 255, 255), pink);
  border-radius: 10px;
  margin: 30px;
}

img {
  border-radius: 30px;
  width: 500px;
  border: 3px solid rgba(112, 199, 255, 255);
}

li{
  text-align: center;
}
</style>
