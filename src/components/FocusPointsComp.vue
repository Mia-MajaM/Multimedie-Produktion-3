<script setup>
import { onMounted } from 'vue';

import FocusPointData from "../assets/data/FocusPointData";

// let currentPageHref = '';

// onMounted(() => {
//   currentPageHref = window.location.href;
// });


</script>
<!-- v-if="card.linkTo == currentPageHref" -->
<template>
  <section class="fpCards">
    <button v-for="card in FocusPointData" :key="card.id" >
      <a :href="card.linkTo" :aria-label="card.ariaLabel"> 
        <h3>{{ card.name }}</h3>
        <img :src="card.imgSrc" :alt="card.alt">
      </a>
    </button>
  </section>
</template>

<style scoped>
  .fpCards {
    display: flex;
    justify-content: center;
    margin-top: 4rem;
  }

  .remove {
    display: none;
  }

  button {
    cursor: pointer;
    width: 15vw;
    margin: 1rem;
    background: none;
    overflow: hidden;
    height: 250px;
    border: 2px solid var(--bordeaux);
    box-shadow: 0 0 0.25rem var(--sort);
    border-radius: 10px;
  }

  button:hover {
    background-color: var(--bordeaux);
  }

  button:hover > a > h3 {
    color: var(--hvid);
  }

  button > a > img {
    width: 100%;
    height: 75%;
    object-fit: cover;
    object-position: top;
  }

  a {
    all: unset;
  }

  h3 {
    text-align: center;
    margin: 1rem;
  }

  img {
    width: 100%;
  }

  @media only screen and (max-width: 391px) {
    .fpCards {
      display: none;
    }
  }
</style>
