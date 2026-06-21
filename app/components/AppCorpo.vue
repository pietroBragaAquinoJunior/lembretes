<script setup lang="ts">


const listaLembrete = reactive(
    [
        { texto: "", id: 1 }
    ]
);

function criarLembrete() {
    listaLembrete.push({ texto: "", id: listaLembrete.length + 1 })
}

defineExpose({
    criarLembrete
})

</script>


<template>
    <div>
        <div class="containerGrid">
            <div class="cartao" key="value.id" v-for="value in listaLembrete">
                <p>{{ value.id }}</p>
                <textarea v-model="value.texto" rows="5" cols="33"></textarea>
            </div>
        </div>
    </div>
    <pre>{{ listaLembrete }}</pre>
</template>

<style lang="css" scoped>
.containerGrid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
}

.cartao {
    border: 1px solid black;
    border-radius: 5px;
    padding: 25px;
}
</style>
