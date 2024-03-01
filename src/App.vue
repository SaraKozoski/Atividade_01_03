<script setup>
 import { ref } from 'vue';
 const contador = ref (0)
  function incrementar() {
    contador.value++
  }
  function decrementar() {
    if (contador.value > 0){
      contador.value --
    }
  }
  function reiniciar(){
    contador.value = 0;
  }
</script>

<template>
   <div>
    <h1>Números</h1>
    <p>{{ contador }}</p>
    <button @click="incrementar">+</button>
    <button @click="decrementar">-</button>
    <button @click="reiniciar">0</button>
   </div>
</template>

<style>
 button{
  background-color: rgb(119, 109, 111);
  color: black;
  margin: 10px;
  width: 100px;
  height: 100px;
  font-size: 20px;
  text-align: center;
 }
 div{
  text-align: center;
 }
 p{
  font-size: 30px;
 }
</style>
