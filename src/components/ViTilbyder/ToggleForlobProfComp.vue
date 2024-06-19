<script setup>
import { ref } from "vue";

// im port af komponenter
import ForlobComp from "../ViTilbyder/ForlobComp.vue"
import ProfessionelComp from "../ViTilbyder/ProfessionelComp.vue"

// States
let forlob = ref(true);
let professionel = ref(false);

// Funktioner der bruges til knapperne.
// hver funktion gør dens eget state true, og andre potentielle states false
const toggleForlob = () => {
  forlob.value = true;
  professionel.value = false;
};

const toggleProfessionel = () => {
  forlob.value = false;
  professionel.value = true;
};
</script>

<template>
  <section class="toggleBtnPlacement">
  <div class="toggleButtons">
    <!-- laver knapper. ved click aktiveres funktionen, der ændre states. -->
    <!-- classen toggleActive bliver tilføjet hvis staten er true -->
    <button class="toggleButtonLeft" @click="toggleForlob" 
    :class="{ 'toggleActive': forlob }" >Forløb</button>

    <button class="toggleButtonRight" @click="toggleProfessionel" 
    :class="{ 'toggleActive': professionel }">Professionel</button>
  </div>
</section>

<!-- Bruger en v-if til at sige, at hvis den pågældende
   state er true, skal componentet vises -->
<ForlobComp v-if="forlob"/>
<ProfessionelComp v-if="professionel"/>
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

  .bookLink{
    text-decoration: underline;
  }

  .linksVidere{
		display: flex;
		justify-content: center;
	}
	.linksVidere>a{
		margin: 0rem 3rem;
	}

	@media only screen and (max-width: 391px) {
		.linksVidere>a{
		margin: 1rem;
	}
  ul{
    padding-left: 1rem;
  }

  a{
    font-size: 1rem;
  }
	}
  </style>