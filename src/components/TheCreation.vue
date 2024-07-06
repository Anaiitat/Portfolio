<script setup>
import Modale from "./TheModale.vue";
import { ref } from "vue";

const creations = [
  {
    id: 1,
    name: "CV",
    image: "CV",
    date: "16-04-2024",
    technologies: "HTML - CSS",
    link: "anaiitat.github.io/CV/",
    description: "",
  },
  {
    id: 2,
    name: "Cahier des charges",
    image: "cahier_des_charges",
    date: "23-04-2024",
    technologies: "PDF",
    link: "",
    description: "",
  },
  {
    id: 3,
    name: "Dynamisme d'un site",
    image: "commentaire",
    date: "28-05-2024",
    technologies: "Java Script",
    link: "anaiitat.github.io/Commentaire/",
    description: "",
  },
];

const revele = ref(false);
const selectedCreation = ref({});
const toggleModale = (creation) => {
  revele.value = !revele.value;
  selectedCreation.value = creation;
};
</script>

<template>
  <section id="creation">
    <h2>Créations</h2>
    <article class="creation_modif">
      <div
        v-for="creation in creations"
        :key="creation.id"
        class="miniature"
        v-on:click="toggleModale(creation)"
      >
        <Modale :reveleModal="revele" :oneCreation="selectedCreation" />
        <img :src="`./src/assets/${creation.image}.png`" />
        <h1>
          {{ creation.name }}
        </h1>
      </div>
    </article>
  </section>
</template>

<style scoped>
h1 {
  border: 2px solid rgba(112, 199, 255, 255);
  background-color: rgba(112, 199, 255, 0.63);
  border-radius: 40px;
  width: 200px;
  text-align: center;
  font-weight: bold;
  margin-top: 10px;
  color: white;
  
}

.creation_modif {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 1000px;
}

.miniature {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 40px;
}

.creation_modif > div > img {
  height: 300px;
  width: 250px;
  opacity: 0.8;
  background-color: aliceblue;
  border-radius: 20px;
}

img:hover {
  transition: transform 0.2s;
  border: 3px solid rgba(112, 199, 255, 255);
}
</style>
