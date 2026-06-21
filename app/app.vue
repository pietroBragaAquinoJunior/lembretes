<script setup lang="ts">
import AppCabecalho from './components/AppCabecalho.vue';
import AppCorpo from './components/AppCorpo.vue';
import { useTemplateRef } from 'vue'
const corpo = useTemplateRef('corpo')


function criarLembrete() {
  corpo.value?.criarLembrete();
}

</script>

<template>
  <div>
    <AppCabecalho @criar-lembrete="criarLembrete" />
    <AppCorpo ref="corpo"/>
  </div>
</template>

<style lang="css">
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
