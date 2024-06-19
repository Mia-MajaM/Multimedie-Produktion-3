<template>
 <button> 
  <a class="bookNuA" target="blank" href="https://system.easypractice.net/book/kjlbye-psykoterapi?cookie_fixed=1#choose-where">Book tid</a>
  </button>
</template>

<style scoped>
button{
position: absolute;
right: 8rem;
width: 9rem;
height: 3.3rem;
background-color: var(--mørkeOrange);
color: var(--hvid);
border-radius: 0 0 30px 30px;
font-size: 1.3rem;
font-weight: 500;
}

@media only screen and (max-width: 391px) {
  button{
    display: none;
  }
}
button:hover{
    background-color: var(--mørkeBlå);
}

.bookNuA{
 all: unset; /* Fjerner alle standardstylingen på a-tagget */
 cursor: pointer;
}


</style>