<template>
  <header>
    <div class="logo">
      <h1>MARKET <span class="swap">Swap</span></h1>
    </div>
    <nav>
      <ul class="menu">
        <li :class="{ active: currentTab === 'catalog' }" @click="catalogClick"><span>Catálogo</span></li>
        <li :class="{ active: currentTab === 'regProduct' }" @click="productClick"><span>Cadastrar Produto</span></li>
        <li :class="{ active: currentTab === 'regCategory' }" @click="categoryClick"><span>Cadastrar Categoria</span></li>
      </ul>
    </nav>
    <div class="fab"><i class="fa-solid fa-bag-shopping"></i></div>
    <img class="userIcon" src="../assets/img64624f77d49397.45271659.jpg" alt="User Photo">
  </header>
</template>

<script>
export default {
  name: 'TopNav',
  data() {
    return {
      currentTab: 'catalog' // Set default tab to 'catalog'
    };
  },
  methods: {
    catalogClick() {
      this.currentTab = 'catalog';
      this.$emit('catalogClick');
    },
    productClick() {
      this.currentTab = 'regProduct';
      this.$emit('productClick');
    },
    categoryClick() {
      this.currentTab = 'regCategory';
      this.$emit('categoryClick');
    }
  }
};
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
    font-size: 30px;
    margin: 0px 60px 0px 10px;
}

.swap {
    font-family: "Dancing Script", cursive;
}

nav {
    width: 70%;
}

.menu li.active {
  background-color: #D1E4FF;
  color: #001d35;
  border-color: #73777f;
}

ul {
    margin-right: 59px;
}

li {
    width: calc(100%/3.3);
    font-size: 16px;
    display: inline;
    padding: 10px;
    float: inline-start;
    border: 1px solid #42474E;
    text-align: center;
    color: #42474E;
}

.menu li:first-child {
    border-radius: 50px 0px 0px 50px;
}

.menu li:last-child {
    border-radius: 0px 50px 50px 0px;
}

.fab {
    width: 42px;
    height: 42px;
    background-color: #D1E4FF;
    color: #42474E;
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