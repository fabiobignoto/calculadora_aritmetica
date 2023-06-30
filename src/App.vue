<script setup>

import { reactive } from 'vue';
import Cabecalho from './components/Cabecalho.vue'
import Formulario from './components/Formulario.vue'
import Resultado from './components/Resultado.vue'


const estado = reactive({
  primeiroNumero: 0,
  segundoNumero: 0,
  operacao: 'soma',

})

function soma() {
  return estado.primeiroNumero + estado.segundoNumero;
}

function subtrai() {
  return estado.primeiroNumero - estado.segundoNumero;
}

function multiplica() {
  return estado.primeiroNumero * estado.segundoNumero;
}

function divide() {
  return estado.primeiroNumero / estado.segundoNumero;
}

function realiza_operacao() {

  switch (estado.operacao) {
    case 'soma': return soma();
    case 'subtrai': return subtrai();
    case 'multiplica': return multiplica();
    case 'divide': return divide();


  }
}

</script>

<template>
  <div class="background p-1 vh-100">

    <Cabecalho />
    <Formulario :primeiro="evento => estado.primeiroNumero = parseInt(evento.target.value)"
      :segundo="evento => estado.segundoNumero = parseInt(evento.target.value)"
      :opera="evento => estado.operacao = evento.target.value" />
    <Resultado :calcula="realiza_operacao()"/>




  </div>
</template>

<style>
select {
  max-width: 80px;
  width: 100%;
}

.background {
  background-color: rgb(230, 230, 230);
}


</style>