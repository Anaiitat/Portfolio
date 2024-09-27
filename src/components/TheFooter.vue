<template>
    <footer>
        <div class="logos">
            <a href="https://github.com/Anaiitat">
                <img src="../assets/github.png" alt="logo github">
            </a>
            <a href="https://www.linkedin.com/in/tatiana-arnaud-171343123/">
                <img src="../assets/linkedin.png" alt="logo linkedin">
            </a>
        </div>
        <div class="date">
            <small>Dernières modification le <time datetime="2024-09-27T16:14+18:00">27/09/2024</time></small>
        </div>
    </footer>
</template>

<style scoped>
footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    background-color: aliceblue;
    border-top: solid rgba(26, 178, 238, 0.158) 2px;
    width: 100%;
    position: relative;
}

.logos {
    display: flex;
    justify-content: center;
    flex: 1;
}

.logos a {
    margin: 0 10px;
}

.logos>a>img:hover {
    transition: transform 0.2s;
    transform: scale(1.2);
}

.date {
    white-space: nowrap;
    position: absolute;
    right: 0;
    color: rgba(112, 199, 255, 255);
    margin: 10px;
}

@media (max-width:768px){

    img{
        width: 40px
    }
    .logos{
        flex:0;
    }
}
</style>