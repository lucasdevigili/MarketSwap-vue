<template>
    <div class="home">
        <NavRail />
    </div>
</template>

<script>
import NavRail from '@/components/NavRail/NavRail.vue'

export default {
    name: 'HomeView',
    components: {
        NavRail
    }
}

</script>

<style scoped>
.home {
    height: 100vh;
    width: 100vw;
    background-color: #F0F4FA;
}
</style>