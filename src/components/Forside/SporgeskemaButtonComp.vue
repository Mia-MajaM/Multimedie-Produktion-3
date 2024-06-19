<template>
<div class="divBtn">
 <button class="btn"><a href="/404"> Spørgeskema </a></button>
</div>
</template>

<style scoped>
a{
 all:unset;
}
.divBtn{
 display: flex;
 justify-content: center;
}
 .btn{
 padding: 1rem;
 text-align: center;
 font-size: 1.3rem;
 background: var(--bordeaux);
 color: var(--hvid);
 border-radius: 40px;
 border: none;
 cursor: pointer;
 animation: bounce 1s ease-in-out infinite;
 margin-bottom: 1rem;
} 

.btn:hover{
    background: var(--hvid);
    color: var(--bordeaux);
    font-weight: 600;
    border: none;
}

@keyframes bounce {
0% {top: 0px;
    transform: translateY(4px);
}
50% {
    transform: translateY(-4px);
  top: -4px;
  -webkit-box-shadow: 0px 10px 13px -7px #000000, 5px 5px 15px 5px rgba(0,0,0,0);
  box-shadow: 0px 10px 13px -7px #000000, 5px 5px 15px 5px rgba(0,0,0,0);
}
100% {top: 0px;
    transform: translateY(4px);
}
}


</style>