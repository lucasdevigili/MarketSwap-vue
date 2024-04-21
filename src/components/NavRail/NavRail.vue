<template>
    <div class="rail">
        <NavRailButton railButton="Home"/>
        <NavRailButton railButton="Buscar"/>
        <NavRailButton railButton="Favoritos"/>
        <NavRailButton railButton="Sobre"/>
    </div>
</template>

<script>
import NavRailButton from './/components/NavRailButton.vue'
    export default {
        name: 'NavRail',
        components: {
            NavRailButton
        }
    }
</script>

<style scoped>
    .rail {
        height: 100%;
        width: min-content;
        background-color: #f9f8fc;
       display: flex;
       flex-direction: column;
       justify-content: center
    }
</style>