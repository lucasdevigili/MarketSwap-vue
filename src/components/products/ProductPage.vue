<template>
    <div class="pCards">
        <div class="smallCard">
            <h2>Eletrônicos:</h2>
            <div class="contents">
                <ProductCards />
                <ProductCards />
                <ProductCards />
                <ProductCards />
            </div>
            <div class="pagination"></div>
        </div>
        <div class="bigCard">
            <div>
                <div>
                    <img src="https://encurtador.com.br/ayLVZ" alt="">
                    <h3>Nome do Produto</h3>
                    <h3>R$00,00</h3>
                    <h6>Categoria</h6>
                </div>
                <p>
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Alias quam commodi, placeat sed sit,
                    obcaecati
                    iste laboriosam ipsum ea porro quaerat adipisci minus quia reprehenderit, expedita aliquid illum.
                    Architecto, incidunt!
                </p>
            </div>
            <div class="buttons">
                <button>Editar</button>
                <button>Excluir</button>
            </div>
        </div>
    </div>
</template>

<script>
import ProductCards from "@/components/products/components/ProductCards.vue"

export default {
    name: 'ProductPage',
    components: {
        ProductCards
    }
}
</script>

<style scoped>
.pCards {
    height: -webkit-fill-available;
    width: 100%;
    background-color: #fdfcff;
    display: flex;
    flex-direction: row;
    border-top: 1px solid #73777F;
}

.smallCard {
    height: 100%;
    width: fit-content;
}

.smallCard h2 {
    color: #1A1C1E;
    font-size: 40px;
    margin: 24px 0 24px 21px;
}

.contents {
    display: flex;
    margin-left: 21px;
}

.bigCard {
    width: 100%;
    border-radius: 12px;
    background-color: #001D35;
    margin: 16px 16px 5px 0;
    color: #F7F2F9;
    font-weight: normal;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.bigCard img {
    height: auto;
    width: 90%;
    margin: 5% 0 19px 5%;
    border-radius: 12px;
}

.bigCard h3 {
    font-size: 20px;
}

.bigCard h6 {
    margin-top: 10px;
}

.bigCard h6,
p {
    font-size: 15px;
}

.bigCard p {
    text-align: justify;
    margin-top: 5%;
}

.bigCard h3,
h6,
p {
    margin: 0 5%;
}

.buttons {
    margin: 0 0 20px 0;
    align-self: self-end;
    margin-right: 21px;
}

.buttons button {
    height: 40px    ;
    width: 111px;
    padding-left: 24px;
    padding-right: 24px;
    border-radius: 50px;
    border: none;
}

.buttons button:first-child {
background-color: #00497A;
color: #ffffff;
margin-right: 12px
}

.buttons button:last-child {
background-color: #d0e4ff;
color: #001d35;
}
</style>