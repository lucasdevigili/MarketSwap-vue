<template>
    <div class="button">
        <div class="icon">
            <i class="fa-solid fa-house" />
        </div>
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
    cursor: pointer;
}

.icon {
    width: 100%;
    padding: 5px 0px 5px 0px;
    text-align: center;
    border-radius: 50px;
}

.icon:hover {
    background-color: #D6E4F7;
    color: #0f1d2a;
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

.button:hover {
    .icon {
        background-color: #D6E4F7;
        color: #0f1d2a;
    }
}
</style>