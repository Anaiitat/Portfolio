<script setup>
import { ref } from "vue";
import emailjs from "@emailjs/browser";

const name = ref("");
const objet = ref("");
const message = ref("");

function sendEmail() {
  emailjs.init(import.meta.env.EMAILJS_PUBLIC_KEY);

  const templateParams = {
    objet: this.objet,
    name: this.name,
    message: this.message,
  };
  const serviceID = import.meta.env.EMAILJS_SERVICEID;
  const templateID = import.meta.env.EMAILJS_TEMPLATEID;
  
  // Envoi du mail
  emailjs.send(serviceID, templateID, templateParams)
  .then(() => {
    alert("E-mail envoyé avec succès");
    // Vide les champs du formulaire
    this.name = "";
    this.objet = "";
    this.message = "";
  }),
    (error) => {
      console.log("Erreur");
    };
}
</script>

<template>
  <section id="contact">
    <h2>Contact</h2>
    <article>
      <form ref="form" @submit.prevent="sendEmail()">
        <ul>
          <li>
            <label for="name">Nom Prénom: </label>
            <input type="text" id="name" v-model="name" />
          </li>
          <li>
            <label for="objet">Objet:</label>
            <input type="text" id="objet" v-model="objet" />
          </li>
          <li>
            <label for="message">Message:</label>
            <textarea type="text" id="message" v-model="message"></textarea>
          </li>
        </ul>
        <button type="submit">Envoyer un message</button>
      </form>
    </article>
  </section>
</template>

<style scoped>
li {
  list-style-type: none;
  margin: 20px;
  display: flex;
  flex-direction: column;
}

ul {
  padding: 0%;
  width: 100%;
  margin: 0%;
  display: flex;
  flex-direction: column;
}

form {
  border: 1px, solid, rgba(112, 199, 255, 255);
  border-radius: 8px;
  padding: 0 25px 0 25px;
  background: white;
  width: 700px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

label {
  color: rgba(112, 199, 255, 255);
  font-weight: bold;
  margin-bottom: 5px;
}

input,
textarea {
  background: hsla(286, 64%, 78%, 0.26);
  border: none;
  border-radius: 5px;
  font-size: 16px;
  box-shadow: 0px 2px 2px 0px rgba(0, 0, 0, 0.25);
  height: 35px;
  width: auto;
  color: rgb(161, 88, 161);
}

input:focus,
textarea:focus {
  outline-color: rgba(112, 199, 255, 255);
}

textarea {
  height: 250px;
}

button {
  color: rgba(112, 199, 255, 255);
  border: none;
  border-radius: 5px;
  font-size: 16px;
  box-shadow: 0px 2px 2px 0px rgba(0, 0, 0, 0.25);
  font-weight: bold;
  margin: 20px;
  padding: 15px;
  width: 200px;
}

button:hover {
  transition: transform 0.2s;
  transform: scale(1.1);
}
</style>
