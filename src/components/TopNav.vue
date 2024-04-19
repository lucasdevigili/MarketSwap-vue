<template>
    <header>
        <div class="logo">
            <h1>MARKET <span class="swap">Swap</span></h1>
        </div>
        <nav>
            <ul class="menu">
                <li><span>Catálogo</span></li>
                <li><span>Cadastrar Produto</span></li>
                <li><span>Cadastrar Categoria</span></li>
            </ul>
        </nav>
        <div class="fab"><i class="fa-solid fa-bag-shopping"></i></div>
        <img class="userIcon" src="../assets/img64624f77d49397.45271659.jpg" alt="User Photo">
    </header>
</template>

<script>
export default {
    name: 'TopNav'
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Days+One&family=Inter:wght@100..900&display=swap');

header {
    height: 15vh;
    width: 100vw;
    background-color: #F9F9FCFA;
    display: flex;
    align-items: center;
    flex-direction: row;
}
h1 {
    width: 100%;
    color: #0062A1;
    font-family: "Days One", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 40px;
    line-height: 50.92px;
    margin: 0px 60px 0px 10px;
}

nav {
    width: 70%;
}

.swap {
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

.menu li:last-child {
    border-radius: 50px 0px 0px 50px;
}

.menu li:first-child {
    border-radius: 0px 50px 50px 0px;
}

li {
    width: calc(100%/3.3);
    font-size: 16px;
    list-style-type: none;
    display: inline;
    padding: 10px;
    float: right;
    border: 1px solid #42474E;
    text-align: center;
    cursor: pointer;
    color: #42474E;
}
.fab {
    width: 42px;
    height: 42px;
    background-color: #D1E4FF;
    margin-right: 20px;
    border-radius: 12px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.fa-bag-shopping {
    height: 18px;
    width: 16px;
    color: #42474E;
}

.userIcon {
    width: 42px;
    height: 42px;
    border-radius: 50px;
    margin-right: 20px;
}

</style>