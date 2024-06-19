<script setup>
import { ref } from "vue";

import AnneKirstineComp from "../OmOs/Dem/AnneKirstineComp.vue";
import KatharinaComp from "../OmOs/Dem/KatharinaComp.vue";
import MortenComp from "../OmOs/Dem/MortenComp.vue";
import KlinikkenComp from "../OmOs/Dem/KlinikkenComp.vue"

let anneKirstine = ref(false);
let katharina = ref(false);
let morten = ref(false);
let klinikken = ref(false);

let popUp = ref(false);

const closePopup = () => {
  popUp.value = false;
};

// Laver en function for hver knap der sætter den ønskede knap til true og de andre til false
const toggleAnneKirstine = () => {
 anneKirstine.value = true;
 katharina.value = false;
 morten.value = false;
 klinikken.value = false;
 popUp.value = true;
};

const toggleKatharina = () => {
 anneKirstine.value = false;
 katharina.value = true;
 morten.value = false;
 klinikken.value = false;
 popUp.value = true;
};

const toggleMorten = () => {
 anneKirstine.value = false;
 katharina.value = false;
 morten.value = true;
 klinikken.value = false;
 popUp.value = true;
};

const toggleKlinikken = () => {
 anneKirstine.value = false;
 katharina.value = false;
 morten.value = false;
 klinikken.value = true;
 popUp.value = true;
};
</script>

<template>
<section class="gridDifferentColumnsInfo">
 <section class="buttonsSection">
  <!-- laver knapper. ved click aktiveres funktionen, der ændre states. -->
  <!-- classen btnActive bliver tilføjet hvis staten er true -->
  <button @click="toggleAnneKirstine">Anne-Kirstine Kiil Kjølbye</button>

  <button @click="toggleKatharina">Katharina Kjølbye Wrist</button>

  <button @click="toggleMorten">Morten Kjølbye</button>
  <button @click="toggleKlinikken">Klinikken</button>
  
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
  <AnneKirstineComp v-if="anneKirstine"/>
  <KatharinaComp v-if="katharina"/>
  <MortenComp v-if="morten"/>
  <KlinikkenComp v-if="klinikken"/>
  </article>
</section>
</template>

<style scoped>

</style>