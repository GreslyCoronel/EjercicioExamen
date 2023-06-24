<script setup>
import { ref , computed } from 'vue';

const numeroCalculadora = ref('');

const agregarNumeros = (numeros) => {
  numeroCalculadora.value += numeros;
}

const calcular = () => {
  numeroCalculadora.value = eval(numeroCalculadora.value);
}

 const eliminar = () =>{
   console.log(0)
}

</script>

<template>
<div class="w-96 h-96 bg-slate-500 mx-auto py-6 mt-8 ">
<input type="text" v-model="numeroCalculadora" class="w-80 bg-black  rounded-md mx-8 h-16  text-white" />
<div>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('1')">1</button>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('2')">2</button>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('3')">3</button>
  <button class="bg-lime-500 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('+')">+</button>
</div>
<div>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('4')">4</button>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('5')">5</button>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('6')">6</button>
  <button class="bg-lime-500 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('-')">-</button>
</div>
<div>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('7')">7</button>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('8')">8</button>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('9')">9</button>
  <button class="bg-lime-500 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('*')">*</button>
</div>
<div>
  <button class="bg-green-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('0')">0</button>
  <button class="bg-red-600 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="eliminar('c')">C</button>
  <button class="bg-yellow-400 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="calcular('=')">=</button>
  <button class="bg-lime-500 h-12 w-16 text-center text-white rounded-md font-bold mx-4 my-3 " @click="agregarNumeros('/')">/</button>
</div>
</div>
</template>

