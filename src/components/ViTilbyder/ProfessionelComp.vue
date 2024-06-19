<script setup>
import { ref } from "vue";

import EgenterapiComp from "../ViTilbyder/Professionel/EgenterapiComp.vue";
import SupervisionComp from "../ViTilbyder/Professionel/SupervisionComp.vue";
import UndervisningComp from "../ViTilbyder/Professionel/UndervisningComp.vue";

let egenterapi = ref(true);
let supervision = ref(false);
let undervisning = ref(false);

let popUp = ref(false);

const closePopup = () => {
  popUp.value = false;
};

// Laver en function for hver knap der sætter den ønskede knap til true og de andre til false
const toggleEgenterapi = () => {
 egenterapi.value = true;
 supervision.value = false;
 undervisning.value = false;
 popUp.value = true;
};

const toggleSupervision = () => {
 egenterapi.value = false;
 supervision.value = true;
 undervisning.value = false;
 popUp.value = true;
};

const toggleUndervisning = () => {
 egenterapi.value = false;
 supervision.value = false;
 undervisning.value = true;
 popUp.value = true;
};
</script>

<template>
<section class="gridDifferentColumnsInfo">
 <section class="buttonsSection">
  <!-- laver knapper. ved click aktiveres funktionen, der ændre states. -->
  <!-- classen btnActive bliver tilføjet hvis staten er true -->
  <button @click="toggleEgenterapi" class="buttonFirst" 
  :class="{ 'btnActive': egenterapi }">Egenterapi</button>

  <button @click="toggleSupervision" 
  :class="{ 'btnActive': supervision }">Supervision</button>

  <button @click="toggleUndervisning" class="buttonLast" 
  :class="{ 'btnActive': undervisning }">Undervisning</button>
  
 </section>
 <!-- Laver en article til at holde indholdet fra componenterne -->
 <!-- Til mobil version tilføjer vi en container til indholdet -->
  <article class="toggleContent" 
  :class="{'toggleContentContainer' : popUp}">

  <!-- Til mobil version tilføjer vi en knap til at lukke containeren-->
  <button class="closeButton" @click="closePopup"><i 
    class="fa-solid fa-xmark"></i></button>

  <!-- Bruger en v-if til at sige, at hvis den pågældende
   state er true, skal componentet vises -->
  <EgenterapiComp v-if="egenterapi"/>
  <SupervisionComp v-if="supervision"/>
  <UndervisningComp v-if="undervisning"/>
  </article>
</section>
</template>

<style scoped>

  </style>