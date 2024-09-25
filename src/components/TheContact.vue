<template>
    <section id="contact">
        <h2>Contact</h2>
        <article>
            <form action="">
                <ul>
                    <li>
                        <label for="name">Nom Prénom:</label>
                        <input type="text" id="name"/>
                    </li>
                    <li>
                        <label for="objet">Objet:</label>
                        <input type="text" id="objet"/>
                    </li>
                    <li>
                        <label for="message">Message:</label>
                        <textarea type="text" id="message"></textarea>
                    </li>
                </ul>
            </form>
            <button type="submit">Envoyer un message</button>
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
    border: 1px, solid, rgba(112, 199, 255, 255);
    border-radius: 10px;
}

#contact > article{
    display: flex;
    flex-direction: column;
    align-items: center;
}

form{
    background-color: rgba(255, 255, 255, 0.534);
    border: 1px, solid, rgba(112, 199, 255, 255);
    border-radius: 8px;
    display: flex;
    width: 700px;
    display: flex;
    margin: 0 25px 0 25px;
    flex-direction: column;
    align-items: center;
}

ul {
  padding: 0%;
  width: 100%;
  margin: 0%;
  display: flex;
  flex-direction: column;
}

li {
  list-style-type: none;
  margin: 20px;
  display: flex;
  flex-direction: column;
  
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
  color: rgb(161, 88, 161);
}

textarea {
  height: 200px;
}

input{
    width: 400px;
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