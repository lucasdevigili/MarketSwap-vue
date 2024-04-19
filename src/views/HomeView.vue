<template>
    <div class="home">
        <TopNav />
        <main>
            <NavRail />
        </main>
    </div>
</template>

<script>
import TopNav from '@/components/TopNav.vue'
import NavRail from '@/components/NavRail/NavRail.vue'

export default {
    name: 'HomeView',
    components: {
        TopNav,
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

main {
    height: 85vh;
}
</style>