<template>
  <div class="pCards">
    <div class="smallCard">
      <h2>Produtos:</h2>
      <div class="contents">
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
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Alias quam commodi, placeat sed sit, obcaecati
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
import ProductCards from "@/components/products/components/ProductCards.vue";

export default {
name: "ProductPage",
components: {
  ProductCards,
},
computed: {
  produtosPorLinhas() {
    const itemsPorLinha = 3;
    const linhas = [];
    for (let i = 0; i < this.listaProdutos.length; i += itemsPorLinha) {
      linhas.push(this.listaProdutos.slice(i, i + itemsPorLinha));
    }
    return linhas;
  },
},
};
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
width: 60% !important;
width: fit-content;
}

.smallCard h2 {
color: #1a1c1e;
font-size: 40px;
margin: 24px 0 24px 21px;
}

.contents {
width: 100%;
display: flex;
flex-wrap: wrap; 
margin-left: 21px;
}

.contents div {
height: 67vh;
display: flex;
flex-wrap: wrap;
justify-content: space-around;
width: 100%;
overflow-y: auto;
}

.bigCard {
width: 34%;
border-radius: 12px;
background-color: #001d35;
margin: 16px 16px 5px 60px;
color: #f7f2f9;
font-weight: normal;
display: flex;
flex-direction: column;
justify-content: space-between;
align-items: center;
}
.bigCard img {
height: auto;
width: 90%;
margin: 5% 0 19px 5%;
border-radius: 12px;
}


.bigCard h3 {
font-size: 20px;
text-align: center;
margin-top: 20px;
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
height: 40px;
width: 111px;
padding-left: 24px;
padding-right: 24px;
border-radius: 50px;
border: none;
}

.buttons button:first-child {
background-color: #00497a;
color: #ffffff;
margin-right: 12px;
}

.buttons button:last-child {
background-color: #d0e4ff;
color: #001d35;
}
</style>