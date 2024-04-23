<template>
  <div>
    <div class="card" v-for="(produto, index) in listaProdutos" :key="index">
      <div id="photo">
        <img :src="produto.img" :alt="`Imagem do Produto ${produto.nome}`" />
      </div>
      <div class="container">
        <div>
          <h3>{{ produto.nome }}</h3>
          <h3>R$ {{ produto.preço }}</h3>
        </div>
        <h6>{{ produto.categoria }}</h6>
      </div>
      <button class="view" @click="handleViewClick(produto)">Visualizar</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCards',
  data() {
    return {
      listaProdutos: []
    };
  },
  created() {
    this.recuperarProdutosDoLocalStorage();
  },
  methods: {
    recuperarProdutosDoLocalStorage() {
      const produtosSalvos = localStorage.getItem('listaProdutos');
      if (produtosSalvos) {
        this.listaProdutos = JSON.parse(produtosSalvos);
      }
    },
    handleViewClick(produto) {
      this.$emit('view-product', produto);
      this.$emit('bigCard')
    }
  }
};
</script>

<style scoped>
.card {
  height: 55vh;
  width: 15vw;
  margin: 0 16px 20px 0;
  background-color: #F0F4FA;
  border: 1px solid #F7F2FA;
  border-radius: 12px;
  box-shadow: 0px 4px 10px -8px rgba(0, 0, 0, 1);
  transition: .5s;
}

.view:hover,
.card:hover {
  box-shadow: 0px 4px 10px -2px rgba(0, 0, 0, .5);
  transition: .5s;
}

#photo {
  height: 55%;
  width: 100%;
}

#photo img {
  height: 100%;
  width: 100%;
  border-radius: 12px;
}

.container {
  height: 20%;
  margin: 10px 0 25px 5px;
}

.container h3 {
  font-size: 16px;
}

.container h6 {
  font-size: 10px;
}

.container h3,
h6 {
  color: #001D35
}

.view {
  height: 40px;
  width: 95%;
  border-radius: 50px;
  border: none;
  margin-left: 5px;
  background-color: white;
  color: #0062a1;
  box-shadow: 0px 4px 10px -8px rgba(0, 0, 0, 1);
  transition: .5s;
}
</style>