<template>
  <div class="centralizar">
    <div class="botao" @click="$emit('criarLembrete')">
        <h2>Lembretes</h2>
        <Icon name="mingcute:plus-line" style="color: black" />
    </div>
  </div>
</template>

<style lang="css" scoped>

.centralizar{
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 25px;
}

.botao{
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
}

.botao:hover{
    border-bottom: 2px solid blue;
}

</style>


