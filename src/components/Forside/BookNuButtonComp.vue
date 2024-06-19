<template>
 <div class="divBtn">
 <button class="btn"> 
  <a target="blank" href="https://system.easypractice.net/book/kjlbye-psykoterapi?cookie_fixed=1#choose-where">Book tid</a>
  </button>
 </div>
</template>

<style scoped>
a{
 all: unset;
}

.divBtn{
 display: flex;
 justify-content: center;
}
.btn{
 padding: 1rem 2rem;
 text-align: center;
 font-size: 1.3rem;
 background: var(--mørkeOrange);
 color: var(--hvid);
 border-radius: 40px;
 border: none;
 cursor: pointer;
 box-shadow: 0.1rem 0.1rem 0.3rem var(--mørkeBlå);
}

.btn:hover{
 background: var(--hvid);
 color: var(--mørkeOrange);
 font-weight: 600;
 border: none;
}
</style>