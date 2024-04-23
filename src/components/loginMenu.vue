<template>
    <body>
    <header>
        <div id="headerContainer">
            <a href="#">
                <h1 class="logo" @click="reload()">Market <span id="swap">Swap</span></h1>
            </a>
        </div>
    </header>
    <section>
        <div id="left">
            <div id="leftContainer">
                <h3>Login</h3>
                <h2>BEM VINDO</h2>
                <p class="logo">Market <span id="swap">Swap</span>
                    <span>, o maior site de venda e troca de produtos do Brasil.</span>
                </p>
            </div>
        </div>
        <div id="right">
            <div id="box">
                <div id="boxContainer">
                    <h2>Bem Vindo</h2>
                    <form action="#">
                        <div id="loginName">
                            <label for="email">
                                E-mail:
                                <input type="email" id="email" class="inpt" />
                                <span id="emailError"></span>
                            </label>
                        </div>
                        <div id="loginPassword">
                            <label for="password">
                                Senha:
                                <input type="password" id="password" class="inpt" required/>
                                <span id="passwordError"></span>
                            </label>
                        </div>
                        <button type="button" @click="validate()">Entrar</button>
                    </form>
                    <div id="line"></div>
                    <label for="remember" id="remember">
                        <input type="checkbox">
                        Lembrar de mim
                    </label>
                    <div id="formOthers">
                        <a href="#">Esqueci a senha</a>
                        <a href="#">Cadastrar-se</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</body>
</template>

<script>
export default {
    name: 'loginMenu',
    methods: {
        validate() {
            document.getElementById("emailError").innerHTML = ""
            document.getElementById("passwordError").innerHTML = ""
            var email = document.getElementById("email").value
            var password = document.getElementById("password").value
            var regEX = /\S+@\S+\.\S+/;

            let statusEmail = false
            let statusPassword = false

            if (email == "") {
                document.getElementById("emailError").innerHTML = "Este item é obrigatório"
            } else {
                if (!regEX.test(email)) {
                    document.getElementById("emailError").innerHTML = "Email inválido!"
                } else {
                    statusEmail = true
                }
            }
            if (password == "") {
                document.getElementById("passwordError").innerHTML = "Este item é obrigatório"
            } else {
                statusPassword = true
            }

            if (statusEmail === true && statusPassword === true) {
                const homePath = '/'
                window.location.href = homePath
            }
        },
        reload() {
            window.location.reload();
        }
    }
}
</script>

<style scoped>

* {
    border: 0;
    margin: 0;
    padding: 0;
    font-family: sans-serif;
}

body {
    height: 100vh;
    width: 100vw;
    background: linear-gradient(45deg, rgba(0, 85, 140, 1) 50%, rgba(46, 172, 253, 1) 100%);
}

header {
    height: 10vh;
    width: 100%;
}

#headerContainer {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

#headerMenu {
    width: 15%;
    display: flex;
    justify-content: center;
}

#headerMenu i {
    font-size: 30px;
    color: white;
    cursor: pointer;
}

#headerMenu i:hover {
    color: rgba(255, 255, 255, 0.5);
}

.logo {
    font-size: 35px;
    font-weight: 100;
    font-family: "Days One", sans-serif;
    font-style: normal;
}

header a {
    text-decoration: none;
    color: white;
}

#swap {
    font-family: "Dancing Script", cursive;
}

section {
    display: flex;
}

#left,
#right {
    height: 90vh;
    width: 50%;
}

#left {
    display: flex;
    justify-content: center;
    color: white;
}

#leftContainer {
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

#leftContainer h3 {
    font-size: 35px;
    font-weight: lighter;
    font-style: italic;
}

#leftContainer h2 {
    font-size: 100px;
    font-weight: bolder;
    font-style: italic;
}

#leftContainer p {
    font-size: 30px;
    width: 70%;
}

#box {
    height: 100%;
    width: 95%;
    background-color: rgb(255, 255, 255);
    border-radius: 5px 5px 0px 0px;
    display: flex;
    justify-content: center;
}

#boxContainer {
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

#boxContainer h2 {
    height: 120px;
    font-size: 70px;
    color: #00558C;
}

#loginName,
#loginPassword {
    margin-bottom: 20px;
}

form label {
    font-size: 20px;
}

form input {
    border: 1px solid gray;
    height: 50px;
    width: 100%;
    border-radius: 10px;
    font-size: 20px;
    padding-left: 5px;
    margin-top: 5px;

}

label span {
    color: red;
    font-size: 15px;
}

#boxContainer button {
    height: 40px;
    width: 100px;
    margin: 10px 0px 30px;
    border-radius: 10px;
    background-color: #6CB45A;
    font-size: 20px;
    color: white;
    transition: 500ms;
    cursor: pointer;
}

#boxContainer button:hover {
    background-color: #278311;
    transition: 500ms;
}

#line {
    height: 2px;
    width: 100%;
    background-color: gray;
    margin-bottom: 10px;
    border-radius: 5px;
}

#remember {
    margin-bottom: 30px;
}

#formOthers {
    display: flex;
    justify-content: space-between;
}

#formOthers a {
    color: black;
    cursor: pointer;
}

#formOthers a:hover {
    color: red;
}

</style>