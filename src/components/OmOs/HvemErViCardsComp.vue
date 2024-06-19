<script setup>
import { ref } from "vue";

import AnneKirstineComp from "../OmOs/Dem/AnneKirstineComp.vue";
import KatharinaComp from "../OmOs/Dem/KatharinaComp.vue";
import MortenComp from "../OmOs/Dem/MortenComp.vue";
import KlinikkenComp from "../OmOs/Dem/KlinikkenComp.vue"

let anneKirstine = ref(false);
let katharina = ref(false);
let morten = ref(false);

// Laver en function for hver knap der sætter den ønskede knap til true og de andre til false
const toggleAnneKirstine = () => {
 anneKirstine.value = !anneKirstine.value;
 katharina.value = false;
 morten.value = false;
};

const toggleKatharina = () => {
 anneKirstine.value = false;
 katharina.value = !katharina.value;
 morten.value = false;
};

const toggleMorten = () => {
 anneKirstine.value = false;
 katharina.value = false;
 morten.value = !morten.value;
};

</script>

<template>
  <section class="flexSection">
<section id="hvemErViCards">
  <div>
 <button @click="toggleAnneKirstine" :class="{ 'btnCardActive': anneKirstine }">
 <h3>Anne-Kirstine Kiil Kjølbye</h3>
 <img src="../../../anne-kirstine-kiil-kjoelbye-psykoterapi.jpg" alt="Anne-Kirstine Kill Kjølbye">
</button>

<button class="buttonMiddel" @click="toggleKatharina" :class="{ 'btnCardActive': katharina }">
 <h3>Katharina Kjølbye Wrist</h3>
 <img src="../../../katharina-kjoelbye-wrist.jpg" alt="Kathrina Kjølbye Wrist">
</button>

<button @click="toggleMorten" :class="{ 'btnCardActive': morten }">
 <h3>Morten Kjølbye</h3>
 <img src="../../../morten-kjoelbye-psykoterapi.jpg" alt="Morten Kjølbye">
</button>
</div>

<div :class="{ 'boxOmOs': anneKirstine || katharina || morten  }">
  <article>
  <AnneKirstineComp v-if="anneKirstine"/>
  <KatharinaComp v-if="katharina"/>
  <MortenComp v-if="morten"/>
  </article>
</div>
</section>
<KlinikkenComp/>
</section>
</template>

<style scoped>
#hvemErViCards{
 display: flex;
 flex-direction: column;
 justify-items: center;
 justify-content: center;
 margin: 4rem 8rem 0rem 8rem;
}

button{
 background: var(--bordeaux);
 border-radius: 50px;
 height: 450px;
 width: 25vw;
 border: 3px  solid var(--bordeaux);
 cursor: pointer;
 overflow: hidden;
 filter: drop-shadow(0 0 0.25rem var(--sort));
}
.buttonMiddel{
  margin: 0rem 3.4rem;
}

img{
width: 100%;
height: 100%;
object-fit: cover;
object-position: center;
border-radius: 0px 0px 50px 50px;
}

.boxOmOs{
  grid-column: span 3;
	border: 3px solid var(--bordeaux);
  border-top: none;
  box-shadow: 0rem 0.1rem 0.1rem var(--mørkeBlå);
  border-radius: 50px;
  width: 82vw;
  display: flex;
  justify-content: center;
}

article{
  display: flex;
  flex-direction: column;
  width: 50vw;
  margin-bottom: 3rem;
  
}

h3{
 color: var(--hvid);
 margin: 2rem 1rem;
 text-align: center;
}

button:hover, 
.btnCardActive{
 background-color: var(--hvid);
}

button:hover > h3,
.btnCardActive>h3{
 color: var(--bordeaux);
}
.hidden{
  display: none;
}
 
</style>