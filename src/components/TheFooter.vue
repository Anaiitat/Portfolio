<template>
    <footer>
      <div></div>
      <div class="logo">
        <a href="https://github.com/Anaiitat" target="_blank">
          <img src="../assets/github.png"/>
        </a>
        <a href="https://www.linkedin.com/in/tatiana-arnaud-171343123/" target="_blank">
          <img src="../assets/linkedin.png"/>
        </a>
        </div>
      <div class="date_modif">
        <small>Dernières modifications le <time datetime="2024-06-28T17:14+18:00">28/06/2024</time> </small>
      </div>
    </footer>
</template>

<style scoped>
footer {
  display: flex;
  justify-content: space-around;
  background-color: aliceblue;
  border-top: solid rgba(26, 178, 238, 0.158) 2px;
  width: 100%;
}

footer > div > a > img {
  height: 50px;
  width: 50px;
  margin: 10px;
}

footer > div > a > img:hover {
  transition: transform 0.2s;
  transform: scale(1.2);
}

.logo {
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.date_modif {
  text-align: end;
  display: flex;
  align-content: flex-end;
  flex-wrap: wrap;
  justify-content: flex-end;
  color: rgb(161, 88, 161);
}
footer > div {
  width: 300px;
}

</style>