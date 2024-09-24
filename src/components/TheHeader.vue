<template>
    <header>
        <div>
            <a>
                <img src="../assets/logo-t.png"/>
            </a>
        </div>
        <nav>
            <a>
                <h1>Présentation</h1>
            </a>
            <a>
                <h1>Créations</h1>
            </a>
            <a>
                <h1>Contact</h1>
            </a>
        </nav>
    </header>
</template>

<style scoped>

header{
    display: flex;
    justify-content: space-between;
    padding: 30px;
    align-items: center;
    border-bottom: solid#a0a5db 2px;
    background-color: aliceblue;
}

img{
    height: 70px;
    margin-left: 10px;
}

nav{
    display: flex;   
    align-items: center;
}

nav > a{
    margin-right: 70px;
    font-size: 18px;
    color: rgba(112, 199, 255, 255);
}

h1{
     font-weight: bold 
}

nav>a:hover{
    transition: transform 0.2s;
    border-bottom: solid 3px ;
}
</style>