<script setup>
import Modale from "./TheModale.vue";
import { ref } from 'vue';

const creations = [
        { 
          id: 1, 
          name: "CV", 
          date: "16-04-2024",
          technologies: "HTML - CSS", 
          link:"anaiitat.github.io/CV/",
          description:"",
        },
        {
          id: 2,
          name: "Cahier des charges",
          date: "23-04-2024", 
          technologies:"PDF",
          link:"",
          description:"",
        },
        {
          id: 3,
          name: "Dynamisme d'un site",
          date: "28-05-2024", 
          technologies: "Java Script",
          link:"anaiitat.github.io/Commentaire/",
          description:"",
        },
];
      
const revele= ref(false);
const selectedCreation = ref({});
const toggleModale = (creation) => {
  revele.value = !revele.value;
  selectedCreation.value = creation;
}   

</script>

<template>
  <section id="creation" >
    <h2>Créations</h2>
    <article class="creation_modif" >
      <div v-for="creation in creations" :key="creation.id" class="miniature" v-on:click="toggleModale(creation)">
        <Modale :reveleModal="revele" :oneCreation="selectedCreation"  />
        <img />
        <h1 >
          {{ creation.name }}
        </h1>
      </div>

    </article>
  </section>
</template>

<style scoped>
.creation_modif {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 600px;
}

.miniature {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.creation_modif > div > img {
  height: 150px;
  width: 150px;
  background-color: aliceblue;
}

/*.miniature:hover {
  transition: transform 0.2s;
  transform: scale(1.2);
}*/


</style>
