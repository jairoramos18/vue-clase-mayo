<script setup>
import { ref } from "vue";

const ischecked = ref(true);
const user = ["jairo", "ana", "pepe", "zoey"]
</script>
<template>
	<ul>
		<li v-for="(usuario,index) in user" :key="index" > {{ index }} {{ usuario }}</li>
	</ul>
  <input type="checkbox" id="check" v-model="ischecked" />
  <label for="check"> pinchame</label>
  <div
    class="bg-blue-500 text-white rounded py-1 px-2"
    :class="{ 'bg-orange-400': ischecked }"
  >
    este es un mensaje
  </div>

  <div v-show="false">este es un mensaje que podria ocultar</div>
  <div v-if="false">este es un mensaje que podria ocultar</div>
  <div v-else>esto se ve porque no se cumplio la condicion del if</div>
</template>
