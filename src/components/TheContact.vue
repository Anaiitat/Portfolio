<template>
    <section id="contact">
        <h2>Contact</h2>
        <article>
          <form>
            <ul>
              <li>
                <label for="name">Nom Prénom: </label>
                <input type="text" id="name" name="user_name" />
              </li>
              <li>
                <label for="objet">Objet:</label>
                <input type="text" id="objet" name="user_objet" />
              </li>
              <li>
                <label for="message">Message:</label>
                <textarea
                  type="text"
                  id="message"
                  name="user_message"
                ></textarea>
              </li>
            </ul>
            <button>Envoyer un Message</button>
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
  width: 500px;
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
  height: 200px;
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