<template>
    <header>
        <div>
            <a href="#header">
                <img src="../assets/logo-t.png" alt="logo t" />
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
    padding: 20px;
    align-items: center;
    border-bottom: solid#a0a5db 2px;
    background-color: aliceblue;
    position: fixed;
    width: 100%;
    z-index: 2;
}

img {
    height: 70px;
    margin-left: 10px;
}

nav {
    display: flex;
    align-items: center;
}

nav>a {
    margin-right: 70px;
    font-size: 18px;
    color: rgba(112, 199, 255, 255);
    text-decoration: none;
}

h1 {
    font-weight: bold
}

nav>a:hover {
    transition: transform 0.2s;
    border-bottom: solid 3px;
}

@media (max-width: 768px) {
    header {
        flex-direction: column;
        padding: 10px;

    }

    nav {
        width: 100%;
        display: flex;
        text-align: center;
        justify-content: space-around;

    }

    nav>a {
        font-size: 10px;
        margin-right: 10px;
        text-align: center;

    }

}
</style>