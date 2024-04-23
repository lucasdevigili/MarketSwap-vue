<template>
    <loginMenu />
</template>

<script>
import loginMenu from '@/components/loginMenu.vue'

export default {
    name: 'LoginView',
    components: {
        loginMenu
    }
}

</script>

<style scoped>
.home {
    height: 100vh;
    width: 100vw;
    background-color: #F0F4FA;


}


main {
    height: 85vh;
}
</style>