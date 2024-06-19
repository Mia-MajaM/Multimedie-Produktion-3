<template>
 <div class="imgBackgroundOm">
	<img class="imgContentOm" src="../../../../morten-kjoelbye-psykoterapi.jpg"/>
</div>
<section class="PopUpContent">
 <h2>Kort om Morten</h2>
 <div class="buttonSectionOm">
<button>
  <a href="/priser">Priser</a>
</button>
<button>
  <a href="/vitilbyder">Vi tilbyder</a>
</button>
 </div>
 <ul>
  <li>Speciallæge i psykiatri</li>
  <li>Godkendt specialist og supervisor i psykoterapi</li>
  <li>Erfaren underviser</li>
  <li>Tidligere lektor ved AAU og AU</li>
 </ul>
 <h2>Mere om Morten</h2>
 <p>Jeg er uddannet speciallæge i psykiatri og godkendt specialist og supervisor i psykoterapi, og har gennem de sidste 35 år arbejdet i psykiatrien, dels i kliniske stillinger, men også i ledelses- og uddannelsesfunktioner.
  <br><br>
  Jeg har tidligere været ansat som klinisk lektor i psykiatri ved såvel Aarhus som Aalborg Universitet både på psykologi- og lægestudiet samt været postgraduat klinisk lektor i psykiatri i Uddannelsesregion Nord. Jeg har siden lægestudiet på Aarhus Universitet arbejdet med mennesker i psykoterapeutisk behandling.
  <br><br>
  I min tid i Risskov var jeg ansat som specialeansvarlig overlæge i psykoterapi og leder af Klinik for Personlighedsforstyrrelser, hvor vi opbyggede det første specialiserede psykoterapeutiske behandlingstilbud til mennesker med borderline personlighedsforstyrrelser.
  <br><br>
  Efter jeg er vendt tilbage til Region Nordjylland, har jeg arbejde som ledende overlæge, cheflæge og senest som uddannelseskoordinerende overlæge ved Psykiatrien.
  <br><br>
  Jeg har gennem mange år været en flittig underviser, behandler og supervisor og er forfatter til flere artikler, bøger og bogkapitler om borderline personlighedsforstyrrelse, mentaliseringsbaseret terapi, psykoanalytisk behandling og supervision.
  <br><br>
  Mit grundsyn er humanistisk og min erfaring er at traumer og tilknytningsrelationer har stor betydning for vores psykiske sundhed.Jeg har undervist og superviseret i psykiatrien, børne & ungdomspsykiatrien, i kommuner og boformer.
</p>

<h2>Morten tilbyder desuden følgende uddannelser:</h2>
<ul>
  <li> Psykoterapiuddannelsen - 3 årig MBT-uddannelse</li>
  <li>Dynamisk mentaliseringsbaseret uddannelse for sygeplejersker</li>
  <li>Supervisionsuddannelse</li>
  <li>Personlighedsforstyrrelser</li>
  <li>Introduktionskursus i mentalisering og MBT</li> 
</ul>
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