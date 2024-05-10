<script setup>
import { ref } from 'vue';

const arreglo =ref(['estudiar bastante', "banana", "platano"])
const nuevoarreglo = ref('')

function add() {
arreglo.value.push(nuevoarreglo.value)
nuevoarreglo.value = ""
}
</script>

<template>
	<div class="border-2 rounded shadow bg-slate-200 max-w-96 mx-auto mt-10 py-6 px-5" >
		
		<div class="flex space-x-2">
			<input v-model="nuevoarreglo" class="w-4/5 outline-none rounded px-2 py-2" placeholder="escribe">
			<button @click="add" class=" bg-green-400 rounded shadow w-1/5">+</button>
		</div>
		<div class="mt-4">
		<div
		v-for="(lista,i) in arreglo" 
		 class=" bg-teal-300 rounded">{{ lista }}</div>
	</div>
	</div>
	
</template>