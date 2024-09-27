<script setup>
import TheModale from'../components/TheModale.vue'
import {ref} from 'vue';

const creations = [
    {
        id:1,
        name: "CV",
        image: "CV",
        date: "16-04-2024",
        technologies: "HTML - CSS",
        link: "https://anaiitat.github.io/CV/",
        link2:"https://github.com/Anaiitat/CV",
        description: "L'objectif etait de créer un CV en HTML et CSS en ligne attrayant et accessible sur différents navigateurs.",
    },
    {
        id: 2,
        name: "Cahier des charges",
        image: "cahier_des_charges",
        date: "23-04-2024",
        technologies: "PDF",
        link: "https://github.com/Anaiitat/Cahier-des-charges-",
        description: "Création du cahier des charges pour la création du site internet de l'entreprise : 'La Socketterie'.",
    },
    {
        id: 3,
        name: "Espace Commentaire",
        image: "commentaire",
        date: "28-05-2024",
        technologies: "Java Script",
        link: "https://anaiitat.github.io/Commentaire/",
        link2:"https://github.com/Anaiitat/Commentaire",
        description: "L'objectif de ce projet était de créer la partie front-end de l'intégration d'un nouveau commentaire dans un espace commentaire.",
    },
]

const revele = ref(false);
const selectedCreation = ref({});

//Ouverture ou fermerture de la modale lorsqu'on clique sur une création
const toggleModale = (creation) => { 
    revele.value = !revele.value;
    selectedCreation.value = creation;

}

</script>


<template>
    <section id="creation">
        <h2>Créations</h2>
        <article>
            <div v-for="creation in creations" :key="creation.id" v-on:click="toggleModale(creation)">
                <TheModale :reveleModale="revele" :theCreation="selectedCreation" />
                <img :src="`./src/assets/${creation.image}.png`" alt="image du projet"/>
                <h3>{{ creation.name }}</h3>
            </div>
        </article>
    </section>
</template>

<style scoped>
h2{
    font-size: 30px;
    margin: 20px;
    padding: 10px;
    font-weight: bold;
    color: rgba(112, 199, 255, 255);
    text-shadow:1px 1px 2px rgb(0, 0, 0) ;
    background-color: rgba(255, 255, 255, 0.863);
    border: 1px solid rgba(112, 199, 255, 1);
    border-radius: 10px;
}

#creation>article{
    display: flex;
    
}

#creation > article > div {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 40px;

}

#creation > article > div > img{
    height:300px;
    width: 250px;
    border-radius: 20px;
}

img:hover{
    transition: transform 0.2s;
    box-shadow: 10px 5px 5px rgba(45, 117, 218, 0.726);
}

h3{
     border: 2px solid rgba(112, 199, 255, 255);
    background-color: rgba(112, 199, 255, 0.63);
    border-radius: 40px;
    width: 200px;
    text-align: center;
    font-weight: bold;
    margin-top: 10px;
    color: white;
}


</style>