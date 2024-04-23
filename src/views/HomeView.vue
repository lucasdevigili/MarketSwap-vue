<template>
    <div class="home">
      <TopNav
        @catalogClick="showCatalog"
        @productClick="showProducts"
        @categoryClick="showCategories"
      />
      <main>
        <NavRail />
        <div class="regProduct" v-if="products">
          <regProductPage />
        </div>
        <div class="regCategory" v-else-if="category">
          <regCategoryPage />
        </div>
        <div class="catalog" v-else>
          <ProductPage />
        </div>
      </main>
    </div>
  </template>
  
  <script>
  import TopNav from '@/components/TopNav.vue';
  import NavRail from '@/components/NavRail/NavRail.vue';
  import ProductPage from '@/components/products/ProductPage.vue';
  import RegProductPage from '@/components/regProductPage.vue';
    import RegCategoryPage from '@/components/regCategoryPage.vue';
  
  export default {
    name: 'HomeView',
    components: {
      TopNav,
      NavRail,
      ProductPage,
      RegProductPage,
      RegCategoryPage
    },
    data() {
      return {
        products: false,
        category: false
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
      },
      showCatalog() {
        this.products = false;
        this.category = false;
      }
    }
  };
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