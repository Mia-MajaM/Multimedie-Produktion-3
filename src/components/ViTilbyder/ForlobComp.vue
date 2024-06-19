<script setup>
import { ref } from "vue";

import TilMandComp from "../ViTilbyder/Forlob/TilMandComp.vue";
import GruppeterapiComp from "../ViTilbyder/Forlob/GruppeterapiComp.vue";
import ParterapiComp from "../ViTilbyder/Forlob/ParterapiComp.vue";
import PsykoedukationComp from "../ViTilbyder/Forlob/PsykoedukationComp.vue";
import StresssamtalerComp from "../ViTilbyder/Forlob/StressamtalerComp.vue";
import UdredningComp from "../ViTilbyder/Forlob/UdredningComp.vue";
import UngesamtalerComp from "../ViTilbyder/Forlob/UngesamtalerComp.vue";

let gruppeterapi = ref(true);
let parterapi = ref(false);
let psykoedukation = ref(false);
let stresssamtaler = ref(false);
let tilMand = ref(false);
let udredning = ref(false);
let ungesamtaler = ref(false);

let popUp = ref(false);

const closePopup = () => {
  popUp.value = false;
};

// Laver en function for hver knap der sætter den ønskede knap til true og de andre til false
const toggleTilMand = () => {
 tilMand.value = true;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 stresssamtaler.value = false;
 udredning.value = false;
 ungesamtaler.value = false;
 popUp.value = true;
};

const toggleGruppeterapi = () => {
 tilMand.value = false;
 gruppeterapi.value = true;
 parterapi.value = false;
 psykoedukation.value = false;
 stresssamtaler.value = false;
 udredning.value = false;
 ungesamtaler.value = false;
 popUp.value = true;
};

const toggleParterapi = () => {
 tilMand.value = false;
 gruppeterapi.value = false;
 parterapi.value = true;
 psykoedukation.value = false;
 stresssamtaler.value = false;
 udredning.value = false;
 ungesamtaler.value = false;
 popUp.value = true;
};

const togglePsykoedukation = () => {
 tilMand.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = true;
 stresssamtaler.value = false;
 udredning.value = false;
 ungesamtaler.value = false;
 popUp.value = true;
};

const toggleStresssamtaler = () => {
 tilMand.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 stresssamtaler.value = true;
 udredning.value = false;
 ungesamtaler.value = false;
 popUp.value = true;
};

const toggleUdredning = () => {
 tilMand.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 stresssamtaler.value = false;
 udredning.value = true;
 ungesamtaler.value = false;
 popUp.value = true;
};

const toggleUngesamtaler = () => {
 tilMand.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 stresssamtaler.value = false;
 udredning.value = false;
 ungesamtaler.value = true;
 popUp.value = true;
};

</script>

<template>
<section class="gridDifferentColumnsInfo">
 <section class="buttonsSection">
  <button @click="toggleGruppeterapi" class="buttonFirst" :class="{ 'btnActive': gruppeterapi }">Gruppeterapi</button>
  <button @click="toggleParterapi" :class="{ 'btnActive': parterapi }">Parterapi</button>
  <button @click="togglePsykoedukation" :class="{ 'btnActive': psykoedukation }">Psykoedukation</button>
  <button @click="toggleStresssamtaler" :class="{ 'btnActive': stresssamtaler }">Stresssamtaler</button>
  <button @click="toggleTilMand"  :class="{ 'btnActive': tilMand }" >Til Mænd</button>
  <button @click="toggleUdredning" :class="{ 'btnActive': udredning }">Udredning</button>
  <button @click="toggleUngesamtaler" class="buttonLast" :class="{ 'btnActive': ungesamtaler }">Ungesamtaler</button>
  
 </section>
 <article class="toggleContent" :class="{'toggleContentContainer' : popUp}">
  <button class="closeButton" @click="closePopup"><i class="fa-solid fa-xmark"></i></button>
 <GruppeterapiComp v-if="gruppeterapi"/>
 <ParterapiComp v-if="parterapi"/>
 <PsykoedukationComp v-if="psykoedukation"/>
 <StresssamtalerComp v-if="stresssamtaler"/>
 <TilMandComp v-if="tilMand"/>
 <UdredningComp v-if="udredning"/>
 <UngesamtalerComp v-if="ungesamtaler"/>
</article>

</section>
</template>

<style scoped>

  </style>