<script setup>
import TheHeader from '../components/TheHeader.vue'
import ThePresentation from '../components/ThePresentation.vue'
import TheCreation from '../components/TheCreation.vue'
</script>

<template>
  <TheHeader />
  <main>
    <h1>Portfolio</h1>
   <ThePresentation />
   <TheCreation />
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Concert+One&display=swap');

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
  margin-top: 104px;
  background-image: url(../assets/particle-lines-futuristic-gradient-background.jpg);
  background-size: cover;
}

main>h1{
  margin-top:20px;
  color: #ffffff;
  font-family: "Concert One", sans-serif;
  font-weight: 400;
  font-style: normal;
  text-shadow: 1px 1px 2px black, 0 0 25px rgb(0, 183, 255), 0 0 25px pink;
  font-size: 80px;
  border: 1px, solid, rgba(112, 199, 255, 255);
  padding: 20px 40px 20px 40px;
  background:linear-gradient(rgba(112, 199, 255, 0.767), rgba(255, 192, 203, 0.767));
  border-radius: 15px 50px 30px;
  
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
  margin: 30px;
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
  font-weight: bold;
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