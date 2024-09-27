<script setup>

//Reception des props de TheCreation.vue
const props = defineProps({
    reveleModale: Boolean,
    theCreation: Object,
})
</script>

<template>
    <div class="bloc-modale" v-if="reveleModale">
        <div class="overlay" v-on:click="toggleModale">
            <div class="modale">
                <button v-on:click="toggleModale">X</button>
                <h3>{{theCreation.name}}</h3>
                <img :src="`./src/assets/${theCreation.image}.png`" alt="image du projet">
                <ul>
                    <li>{{ theCreation.date }}</li>
                    <li>{{ theCreation.technologies }}</li>
                    <li class="barre"></li>
                    <li>{{ theCreation.description }}</li>
                    <li class="barre"></li>
                    <li><a :href="theCreation.link">{{ theCreation.link }}</a></li>
                    <li><a :href="theCreation.link2">{{ theCreation.link2 }}</a></li>

                </ul>
                
            </div>
        </div>
    </div>
</template>

<style scoped>
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
  border-radius: 20px;
}

.modale > button{
    position: absolute;
    top: 10px;
    right: 10px;
}

h3 {
  font-weight: bold;
  margin: 10px;
  font-size: 40px;
  color: rgb(255, 255, 255);
  text-shadow: 1px 1px 2px black;
  border: 1px solid rgba(112, 199, 255, 1);
  padding: 5px 10px 10px 10px;
  background: linear-gradient(rgba(112, 199, 255, 255), pink);
  border-radius: 15px 50px 30px;
  writing-mode: vertical-rl;
  text-align: center;
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

@media (max-width:768px){
  .modale{
    flex-direction: column;
    align-items: center;
    max-width: 1000px;
  }

  img{
    width: 250px;
  }

  h3{
    writing-mode: horizontal-tb;
  }

  li{
    text-align: center;
    font-size: 10px;
  }

  button{
    margin-right: 50px;
  }
}

</style>