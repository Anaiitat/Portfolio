<script setup>
</script>

<template>
    <header>
        <div>
      <a href="@\portfolio\index.html">
        <img src="../assets/network.png" alt="" />
      </a>
    </div>
    <nav>
      <a href="#presentation">
        <h1>Présentation</h1>
      </a>
      <a href="#creation">
        <h1>Créations</h1>
      </a>
      <a href="#contact">
        <h1>Contact</h1>
      </a>
    </nav>
    </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  border-bottom: solid rgba(26, 178, 238, 0.158) 2px;
  position: fixed;
  width: 100%;
  z-index: 2;
  background-color: aliceblue;
}

h1 {
  font-weight: bold;
}

img {
  height: 70px;
}

div {
  margin: 20px 10px 10px 20px;
  width: auto;
}
nav > a {
  margin: 20px;
  color: rgba(112, 199, 255, 255);
}

nav > a > h1:hover {
  transition: transform 0.2s;
  transform: scale(1.2);
}

nav {
  display: flex;
  align-items: center;
}
</style>