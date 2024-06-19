<template>
  <div class="imgBackgroundOm">
	<img class="imgContentOm" src="../../../../katharina-kjoelbye-wrist.jpg"/>
</div>
<section class="PopUpContent">
 <h2>Kort om Kathrina</h2>
 <div class="buttonSectionOm">
<button>
  <a href="/priser">Priser</a>
</button>
<button>
  <a href="/vitilbyder">Vi tilbyder</a>
</button>
 </div>
 <ul>
  <li>Autoriseret Psykolog</li>
  <li>Certificeret MBT terapeut</li>
  <li>På vej mod specialist i psykoterapi</li>
  <li>Behandlingserfaring</li>
  <li>Udredningserfaring</li>
  </ul>

  <h2>Mere om Katharina</h2>
  <p>Jeg er uddannet psykolog fra Aalborg Universitet i 2016, og har arbejdet som psykolog i psykiatrien i 7 år, både i Lokalpsykiatrien Middelfart og Ambulatorium for Angst- og Personlighedspsykiatri i Brønderslev.</p>
  <p>Jeg har blandt andet arbejdet med og har efering indenfor udredning, behandling (individuelt og i gruppe) og undervisningserfaring. Jeg tilbyder psykoligske undersøgeser indenfor blandt andet:</p>
  <ul>
   <li>Personlighedsforstyrrelser</li>
   <li>Autisme spektrum forstyrrelser</li>
   <li>Affektive lidelser (depression, mani, bipolar lidelse)</li>
   <li>Tilpasningsreaktion (belastningsreaktioner)</li>
   <li>Angstlidelser (socialangst, panikangst, agorafobi, PTSD, OCD)</li>
   <li>Stress</li>
   <li>ADHD</li>
   <li>Spiseforstyrrelse</li>
   <li>Mennesker i sorg og krise</li>
   <li>Begavelse/IQ - bl.a. WAIS-IV-testning</li>
   </ul>
   <p>Du er velkommen til at kontakte mig for nærmere information vedrørende udredning og eventuel aftale om et udredende forløb.</p>
</section>
</template>

<style scoped>
h2{
  margin-top: 2rem;
  text-align: center;
}

ul{
    padding-left: 2rem;
  }

@media only screen and (max-width: 391px) {
  h2{
    margin-top: 1rem;
  }
  ul{
    padding-left: 1rem;
  }
}

a{
  all: unset;
}

button{
 padding: 1rem;
 margin: 2rem 4rem;
 width: 10vw;
 text-align: center;
 font-size: 1.3rem;
 background: var(--bordeaux);
 color: var(--hvid);
 border-radius: 40px;
 cursor: pointer;
} 

button:hover{
    background: var(--hvid);
    color: var(--bordeaux);
    font-weight: 600;
}

.buttonSection{
  display: flex;
  justify-content: center;
}

</style>