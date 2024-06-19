<script setup>
import { ref } from "vue";

import PriserAnneKirstineComp from "../Priser/Pris/PriserAnneKirstineComp.vue";
import PriserKatharinaComp from "../Priser/Pris/PriserKatharinaComp.vue";
import PriserMortenComp from "../Priser/Pris/PriserMortenComp.vue";
import AfbudComp from "../Priser/Pris/AfbudComp.vue";
import Gruppe2Comp from "../Priser/Pris/Gruppe2Comp.vue";
import BetalingComp from "../Priser/Pris/BetalingComp.vue";

let anneKirstine = ref(false);
let katharina = ref(false);
let morten = ref(false);
let afbud = ref(false);
let gruppe2 = ref(false);
let betaling = ref(false);

// Laver en function for hver knap
const toggleAnneKirstine = () => {
 anneKirstine.value = !anneKirstine.value;
};
const toggleKatharina = () => {
 katharina.value = !katharina.value;
};
const toggleMorten = () => {
 morten.value = !morten.value;
};
const toggleAfbud = () => {
 afbud.value = !afbud.value;
};
const toggleGruppe2 = () => {
 gruppe2.value = !gruppe2.value;
};
const toggleBetaling = () => {
 betaling.value = !betaling.value;
};

</script>

<template>
	<section class="flexSection">
  <button @click="toggleAnneKirstine">Priser Anne Kirstine Kill Kjølbye 
			<i class="fa-solid fa-chevron-down" :class="{'rotateChevron' : anneKirstine}"></i></button>
		<article :class="{'boxPriser': anneKirstine}">
				<PriserAnneKirstineComp v-if="anneKirstine"/>
		</article>

  <button @click="toggleKatharina">Priser Katharina Kjølbye Wrist 
			<i class="fa-solid fa-chevron-down" :class="{'rotateChevron' : katharina}"></i></button>
		<article :class="{'boxPriser': katharina}">
				<PriserKatharinaComp v-if="katharina"/>
		</article>

  <button @click="toggleMorten">Priser Morten Kjølbye 
			<i class="fa-solid fa-chevron-down" :class="{'rotateChevron' : morten}"></i></button>
		<article :class="{'boxPriser': morten}">
				<PriserMortenComp v-if="morten"/>
		</article>

  <button @click="toggleAfbud">Afbud og udeblivelse 
			<i class="fa-solid fa-chevron-down" :class="{'rotateChevron' : afbud}"></i></button>
		<article :class="{'boxPriser': afbud}">
				<AfbudComp v-if="afbud"/>
		</article>

  <button @click="toggleGruppe2">Gruppe 2 sikrede 
			<i class="fa-solid fa-chevron-down" :class="{'rotateChevron' : gruppe2}"></i></button>
		<article :class="{'boxPriser': gruppe2}">
				<Gruppe2Comp v-if="gruppe2"/>
		</article>

  <button @click="toggleBetaling">Betaling 
			<i class="fa-solid fa-chevron-down" :class="{'rotateChevron' : betaling}"></i></button>
		<article :class="{'boxPriser': betaling}">
				<BetalingComp v-if="betaling"/>
		</article>
  
	</section>

</template>

<style scoped>
	.h2{
 text-align: center;
}
 </style>