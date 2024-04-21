<template>
<div class="card">
    <div id="caixa">
    </div>
    <div>
<h3>Nome do Produto</h3>
<h3>Preço</h3>
<h6>Categoria</h6>
    </div>
</div>
</template>

<script>
export default {
    name: 'ProductCards'
}
</script>

<style scoped>

.card {
    widows: 205px;
    height: 287px;
    
    border-color: black;

}
#caixa {
    width: 205px;
    height: 205px;
    background-color: gray;
    border-radius: 12px;
}



</style>