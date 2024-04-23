<template>
  <div class="pRegister">
    <div class="title">
      <h2>Registrar novo produto:</h2>
    </div>
    <form @submit.prevent="addProduct">
      <div class="formContents">
        <div class="inptContainner">
          <label class="label">Nome:</label>
          <input type="text" v-model="novoProduto.nome">
          <span>Error</span>
        </div>

        <div class="inptContainner">
          <label class="label">Categoria:</label>
          <input type="text" v-model="novoProduto.categoria">
          <span>Error</span>
        </div>

        <div class="inptContainner">
          <label class="label">Preço:</label>
          <input type="text" v-model="novoProduto.preço">
          <span>Error</span>
        </div>

        <div class="inptContainner">
          <label class="label">Enviar Imagem: </label>
          <input type="text" v-model="novoProduto.img"/>
          <span>Error</span>
        </div>

        <div class="inptContainner">
          <label class="label">Descrição:</label>
          <textarea v-model="novoProduto.descrição" name="descrição" id="descript" cols="160" rows="10"></textarea>
          <span>Error</span>
        </div>

        <div class="buttons">
          <button type="button" @click="limparListaProdutos">Cancelar</button>
          <button type="submit">Adicionar</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "regProductPage",
  data() {
    return {
      novoProduto: {
        nome: "",
        categoria: "",
        preço: "",
        img: "",
        descrição: ""
      },
      listaProdutos: []
    };
  },
  mounted() {
    this.getLS();
  },
  methods: {
    addProduct() {
      this.listaProdutos.push(JSON.parse(JSON.stringify(this.novoProduto)));
      localStorage.setItem("listaProdutos", JSON.stringify(this.listaProdutos));
      this.limparNovoProduto();

      console.log("Novo produto adicionado e salvo no localStorage!");
    },
    limparNovoProduto() {
      this.novoProduto = {
        nome: "",
        categoria: "",
        preço: "",
        img: "",
        descrição: ""
      };
    },
    limparListaProdutos() {
      localStorage.removeItem("listaProdutos");
      this.listaProdutos = [];
      console.log("Lista de produtos removida do localStorage!");
    },
    getLS() {
      const produtosSalvos = localStorage.getItem("listaProdutos");
      if (produtosSalvos) {
        this.listaProdutos = JSON.parse(produtosSalvos);
      }
    }
  }
};
</script>


<style scoped>
.pRegister {
  height: -webkit-fill-available;
  background-color: #fdfcff;
  border-top: 1px solid #73777F;
}

.title h2 {
  color: #1A1C1E;
  font-size: 40px;
  margin: 24px 0 50px 21px;
}

form {
  margin: 0 21px;
}

.inptContainner {
  display: flex;
  flex-direction: column;
  width: calc(100% / 2.02);
}

.inptContainner input {
  height: 40px;
  padding-left: 10px;
  font-size: 20px;
  border-radius: 5px;
  border: 1px solid #73777f;
}

.inptContainner textarea {
  resize: none;
  padding: 10px 0 0 10px;
}

.inptContainner span {
  font-size: 12px;
  color: #ba1a1a;
}

.fa-file-arrow-up {
  font-size: 20px;
}

.formContents {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.buttons {
  width: calc(100% / 2.02);
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  gap: 10px;
}

.buttons button {
  height: 40px;
  width: 100px;
  padding: 0 24px 0 24px;
  border-radius: 50px;
  border: none;
}

.buttons button:first-child {
  background-color: transparent;
  color: #0062a1;
}

.buttons button:last-child {
  background-color: #0062a1;
  color: #ffffff;
}
</style>