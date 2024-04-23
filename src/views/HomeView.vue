<template>
    <div class="home">
      <TopNav />
      <main>
        <NavRail />
        <div class="regProduct" v-if="products">
          <regProductPage />
        </div>
        <div class="regProduct" v-else-if="category">
          <regCategoryPage />
        </div>
        <div class="catalog" v-else>
          <ProductPage />
        </div>
      </main>
    </div>
  </template>
  
  <script>
  import TopNav from '@/components/TopNav.vue'
  import NavRail from '@/components/NavRail/NavRail.vue'
  import ProductPage from '@/components/products/ProductPage.vue'
  import regProductPage from '@/components/regProductPage.vue'
  import regCategoryPage from "@/components/regCategoryPage.vue";
  
  export default {
    name: 'HomeView',
    components: {
      TopNav,
      NavRail,
      ProductPage,
      regProductPage,
      regCategoryPage
    },
    data() {
      return {
        products: false,
        category: true
      };
    },
    methods: {
      showProducts() {
        this.products = true;
        this.category = false;
      },
      showCategories() {
        this.category = true;
        this.products = false;
      }
    }
  }
  </script>
  
  <style scoped>
  .home {
    height: 100vh;
    width: 100vw;
  }
  
  main {
    height: 85vh;
    width: 100%;
    display: flex;
  }
  
  .regProduct {
    width: 100%;
  }
  </style>
  