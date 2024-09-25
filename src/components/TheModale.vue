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
  width: 1000px;
  border-radius: 20px;
}

.modale > button{
    position: absolute;
    top: 10px;
    right: 10px;
}
</style>