<template>
    <header>
        <h1>MARKET <span id="swap">Swap</span></h1>

        <nav>
            <ul>
                <li><span>Catálogo</span></li>
                <li><span>Cadastrar Produto</span></li>
                <li><span>Cadastrar Categoria</span></li>
            </ul>
        </nav>
        <div id="quadradoBoludo"></div>
        <img class="bola" src="../assets/img64624f77d49397.45271659.jpg" alt="User Photo">



    </header>

    <div id="card">
        <img src="" alt="">
        <div id="container">
            <h3>Nome do Produto</h3>
            <h3>Preço</h3>
            <p>Categoria</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TopNav'
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Days+One&family=Inter:wght@100..900&display=swap');

header {
    width: 100vw;
    height: 88px;
    background-color: #F9F9FCFA;
    display: flex;
    align-items: center;
    flex-direction: row;
}

li {
    font-family: "Inter", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-size: 16px;
    font-style: normal;
    line-height: 19.36px;
    font-variation-settings:
        "slnt" 0;
    list-style-type: none;
    display: inline;
    padding: 10px;
    float: right;
    border: 1px solid black;
}

.bola {
    width: 40px;
    height: 40px;
    border-radius: 50px;


}

#quadradoBoludo {
    width: 40px;
    height: 40px;
    top: 24px;
    background-color: #D1E4FF;
    margin-right: 9px;
    
    border-radius: 12px;
    

}




h1 {
    color: #0062A1;
    font-family: "Days One", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 40px;
    line-height: 50.92px;
    margin: 0px 59px 0px 9px;
}

#swap {

    font-family: "Dancing Script", cursive;
    font-optical-sizing: auto;
    font-weight: 400;
    font-size: 40px;
    font-style: normal;
    line-height: 48px;
}

ul {
    margin-right: 59px;
}
</style>