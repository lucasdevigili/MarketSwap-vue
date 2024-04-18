<template>
    <div class="button">
        <i class="fa-solid fa-house"></i>
        <p>{{ railButton }}</p>
    </div>
</template>

<script>
    export default {
        name: 'NavRailButton',
        props: {
            railButton: String
        }
    }
</script>

<style scoped>
    .button {
        height: 56px;
        width: 76px;
        margin: 0px 5px 0px 5px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .fa-house {
        height: 18px;
        width: 16px;
        color: #42474E;
    }

    .button p {
        font-size: 12px;
        color: #42474E;
    }
</style>