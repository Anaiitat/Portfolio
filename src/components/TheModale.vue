<script setup>
const props = defineProps({
  reveleModal: Boolean,
  oneCreation: Object
});
</script>


<template>
  <div class="bloc-modale" v-if="reveleModal" >
    <div class="overlay" v-on:click="toggleModale">
      <div class="modale">
        <button  v-on:click="toggleModale" class="btn-modale btn btn-danger">X</button>
        <h1>{{ oneCreation.name }}</h1>
        <img />

        <ul>
          <li>Date de création</li>
          <li>Description du projet</li>
          <li>Technologies utilisé</li>
          <li>
            lien pour visiter le site ou le fichier PDF (dans un nouvelle
            onglet)
          </li>
          <li>un lien vers le repository Github</li>
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
  padding: 50px;
  position: fixed;
  top: 30%;
   z-index: 2;
}
.btn-modale {
  position: absolute;
  top: 10px;
  right: 10px;
}
</style>
