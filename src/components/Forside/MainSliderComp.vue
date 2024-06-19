<template>
 <!-- prøve at følg denne video: https://www.youtube.com/watch?v=qDww4CbxtD4 -->
<div id="image-slider">
  <figure>
  <img src="../../../ungesamtaler.jpg" alt="Billede af en mand til psykoterapi">
  <img src="../../../venteværelse.jpg" alt="Billede af en mand til psykoterapi">
  <img src="../../../egenterapi_og_udredning.jpg" alt="Billede af en mand til psykoterapi">
  <img src="../../../ungesamtaler.jpg" alt="Billede af en mand til psykoterapi">
</figure>
</div>
</template>

<script setup>
</script>

<style scoped>
#image-slider{
 overflow: hidden;
 margin: 0rem 8rem; 
}

figure{
 position: relative;
 width: 400%;
 height: 400px;
 margin: 0;
 left: 0;
 animation: 20s slider infinite;
}

img{
 float: left;
 width: 25%;
 border-radius: 0px 0px 10px 10px;
 height: 100%;
 object-fit: cover;
 object-position: center;
}

@media only screen and (max-width: 391px) {
  #image-slider{
 margin: 0rem 0rem; 
}

figure{
 height: 200px;
}
img{
 border-radius: 0px;
}
}

@keyframes slider{
0% {
  left: 0;
}

13% {
  left: 0;
}

33% {
  left: -100%;
}

46% {
  left: -100%;
}

66% {
  left: -200%;
}

80% {
  left: -200%;
}

100% {
  left: -300%;
}

}
</style>