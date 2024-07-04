<script setup>
import TheHeader from '../components/TheHeader.vue'
import ThePresentation from '../components/ThePresentation.vue'
</script>

<template>
  <TheHeader />
  <main>
   <ThePresentation />
  </main>
</template>

<style>
body {
  display: flex;
  flex-direction: column;
  margin: 0%;
}
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  margin-top: 114px;
  background-image: url(../assets/particle-lines-futuristic-gradient-background.jpg);
  background-size: cover;
}

h1,
h2,
a,
p,
label,
textarea,
button,
input,
small {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica,
    Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}

section {
  border: 2px solid rgba(112, 199, 255, 255);
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 20px;
  margin: 20px;
}

h2 {
  color: rgba(112, 199, 255, 255);
  border: 1px, solid, rgba(112, 199, 255, 255);
  background-color: white;
  display: flex;
  justify-content: space-evenly;
  width: 250px;
  border-radius: 10px;
  margin: 10px;
  padding: 8px;
}

article {
  margin: 20px;
}

#presentation,
#creation,
#contact {
  scroll-margin-top: 114px;
}
</style>