<script setup  >
import { ref } from 'vue';

const ischecked = ref(false)
</script>
<template>
 
<div>
	<input type="checkbox" id="check" v-model="ischecked">
 <label for="check"> pinchame</label>

</div>
	 <div v-show="false">
		este es un mensaje que podria ocultar
	</div>
	<div v-if="false">
		este es un mensaje que podria ocultar
	</div>
	<div v-else>
		esto se ve porque no se cumplio la condicion del if
	</div> 

 
</template>