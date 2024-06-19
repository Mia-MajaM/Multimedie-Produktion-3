<script setup>
import { ref } from "vue";

import KlientComp from "../Selvhjaelp/KlientComp.vue"
import PaarorendeComp from "../Selvhjaelp/PaarorendeComp.vue"

let klient = ref(true);
let paarorende = ref(false);


const toggleKlient = () => {
  klient.value = true;
  paarorende.value = false;
};

const togglePaarorende = () => {
  klient.value = false;
  paarorende.value = true;
};

</script>

<template>
  <section class="toggleBtnPlacement">
  <div class="toggleButtons">
    <!-- laver knapper. ved click aktiveres funktionen, der ændre states. -->
    <!-- classen toggleActive bliver tilføjet hvis staten er true -->
    <button class="toggleButtonLeft" @click="toggleKlient" :class="{ 'toggleActive': klient }" >Klient</button>
    <button class="toggleButtonRight" @click="togglePaarorende" :class="{ 'toggleActive': paarorende }">Pårørende</button>
  </div>
</section>

<KlientComp v-if="klient"/>
<PaarorendeComp v-if="paarorende"/>
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