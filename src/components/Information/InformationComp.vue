<script setup>
import { ref } from "vue";

import EgenterapiComp from "../Information/Info/EgenterapiComp.vue";
import GruppeterapiComp from "../Information/Info/GruppeterapiComp.vue";
import ParterapiComp from "../Information/Info/ParterapiComp.vue";
import PsykoedukationComp from "../Information/Info/PsykoedukationComp.vue";
import PsykoterapiComp from "../Information/Info/PsykoterapiComp.vue";
import StresssamtalerComp from "../Information/Info/StresssamtalerComp.vue";
import SupervisionComp from "../Information/Info/SupervisionComp.vue";
import TilMandComp from "../Information/Info/TilMandComp.vue";
import UdredningComp from "../Information/Info/UdredningComp.vue";
import UndervisningComp from "../Information/Info/UndervisningComp.vue";
import UngesamtalerComp from "../Information/Info/UngesamtalerComp.vue";

let egenterapi = ref(false);
let gruppeterapi = ref(false);
let parterapi = ref(false);
let psykoedukation = ref(false);
let psykoterapi = ref(true);
let stresssamtaler = ref(false);
let supervision = ref(false);
let tilMand = ref(false);
let udredning = ref(false);
let undervisning = ref(false);
let ungesamtaler = ref(false);

// Laver en function for hver knap der sætter den ønskede knap til true og de andre til false
const toggleEgenterapi = () => {
 egenterapi.value = true;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleGruppeterapi = () => {
 egenterapi.value = false;
 gruppeterapi.value = true;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleParterapi = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = true;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const togglePsykoedukation = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = true;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const togglePsykoterapi = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = true;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleStresssamtaler = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = true;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleSupervision = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = true;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleTilMand = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = true;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleUdredning = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = true;
 undervisning.value = false;
 ungesamtaler.value = false;
};

const toggleUndervisning = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = true;
 ungesamtaler.value = false;
};

const toggleUngesamtaler = () => {
 egenterapi.value = false;
 gruppeterapi.value = false;
 parterapi.value = false;
 psykoedukation.value = false;
 psykoterapi.value = false;
 stresssamtaler.value = false;
 supervision.value = false;
 tilMand.value = false;
 udredning.value = false;
 undervisning.value = false;
 ungesamtaler.value = true;
};

</script>

<template>
<section class="gridDifferentColumnsInfo">
 <section class="buttonsSection">
  <button @click="togglePsykoterapi" class="buttonFirst" :class="{ 'btnActive': psykoterapi }">Psykoterapi</button>
  <button @click="toggleEgenterapi" :class="{ 'btnActive': egenterapi }">Egenterapi</button>
  <button @click="toggleGruppeterapi" :class="{ 'btnActive': gruppeterapi }">Gruppeterapi</button>
  <button @click="toggleParterapi" :class="{ 'btnActive': parterapi }">Parterapi</button>
  <button @click="togglePsykoedukation" :class="{ 'btnActive': psykoedukation }">Psykoedukation</button>
  <button @click="toggleStresssamtaler" :class="{ 'btnActive': stresssamtaler }">Stresssamtaler</button>
  <button @click="toggleSupervision" :class="{ 'btnActive': supervision }">Supervision</button>
  <button @click="toggleTilMand" :class="{ 'btnActive': tilMand }">Til Mænd</button>
  <button @click="toggleUdredning" :class="{ 'btnActive': udredning }">Udredning</button>
  <button @click="toggleUndervisning" :class="{ 'btnActive': undervisning }">Undervisning</button>
  <button @click="toggleUngesamtaler" class="buttonLast" :class="{ 'btnActive': ungesamtaler }">Ungesamtaler</button>
  </section>

  <article class="toggleContent">
 <EgenterapiComp v-if="egenterapi"/>
 <GruppeterapiComp v-if="gruppeterapi"/>
 <ParterapiComp v-if="parterapi"/>
 <PsykoedukationComp v-if="psykoedukation"/>
 <PsykoterapiComp  v-if="psykoterapi"/>
 <StresssamtalerComp v-if="stresssamtaler"/>
 <SupervisionComp v-if="supervision"/>
 <TilMandComp v-if="tilMand"/>
 <UdredningComp v-if="udredning"/>
 <UndervisningComp v-if="undervisning"/>
 <UngesamtalerComp v-if="ungesamtaler"/>
</article>

</section>
</template>

<style>
  a{
	color: var(--mørkeBlå);
	text-decoration: none;
	font-weight: 500;
  font-size: 1.3rem;
  line-height: 1.5;
  margin-bottom: 1rem;
	}

	a:hover{
		color: var(--bordeaux);
	}

  ul{
    padding-left: 2rem;
  }

  @media only screen and (max-width: 391px) {
  ul{
    padding-left: 1rem;
  }

  a{
    font-size: 1rem;
  }
	}
  </style>