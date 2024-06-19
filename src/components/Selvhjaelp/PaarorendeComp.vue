<script setup>
import { ref } from "vue";

import AngstComp from "../Selvhjaelp/Paarorende/AngstComp.vue";
import DepressionComp from "../Selvhjaelp/Paarorende/DepressionComp.vue";
import LavtSelvvardComp from "../Selvhjaelp/Paarorende/LavtSelvvardComp.vue";
import SelvskadeComp from "../Selvhjaelp/Paarorende/SelvskadeComp.vue";
import StressComp from "../Selvhjaelp/Paarorende/StressComp.vue";


let angst = ref(true);
let depression = ref(false);
let lavtSelvvard = ref(false);
let selvskade = ref(false);
let stress = ref(false);

// Laver en function for hver knap der sætter den ønskede knap til true og de andre til false
const toggleAngst = () => {
 angst.value = true;
 depression.value = false;
 lavtSelvvard.value = false;
 selvskade.value = false;
 stress.value = false;
};

const toggleDepression = () => {
 angst.value = false;
 depression.value = true;
 lavtSelvvard.value = false;
 selvskade.value = false;
 stress.value = false;
};

const toggleLavtSelvvard = () => {
 angst.value = false;
 depression.value = false;
 lavtSelvvard.value = true;
 selvskade.value = false;
 stress.value = false;
};

const toggleSelvskade = () => {
 angst.value = false;
 depression.value = false;
 lavtSelvvard.value = false;
 selvskade.value = true;
 stress.value = false;
};

const toggleStress = () => {
 angst.value = false;
 depression.value = false;
 lavtSelvvard.value = false;
 selvskade.value = false;
 stress.value = true;
};

</script>

<template>
<section class="gridDifferentColumnsInfo">
 <section class="buttonsSection">
  <button @click="toggleAngst" class="buttonFirst" :class="{ 'btnActive': angst }" >Angst</button>
  <button @click="toggleDepression" :class="{ 'btnActive': depression }">Depression</button>
  <button @click="toggleLavtSelvvard" :class="{ 'btnActive': lavtSelvvard }">Lavt selvværd</button>
  <button @click="toggleSelvskade" :class="{ 'btnActive': selvskade }">Selvskade</button>
  <button @click="toggleStress" class="buttonLast" :class="{ 'btnActive': stress }">Stress</button>
 </section>

<article class="toggleContent">
 <AngstComp v-if="angst"/>
 <DepressionComp v-if="depression"/>
 <LavtSelvvardComp v-if="lavtSelvvard"/>
 <SelvskadeComp v-if="selvskade"/>
 <StressComp v-if="stress"/>
</article>

</section>
</template>

<style scoped>

  </style>