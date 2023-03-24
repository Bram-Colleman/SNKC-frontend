<script setup>

</script>

<template>
  <div class="activityContainer">
    <h1>Kumite</h1>
    <p class="inleiding">Kumite is een vorm van trainen met partner. In kata bestaat de tegenstander alleen in de verbeelding maar in kumite wordt er geoefend met een echte tegenstander. De bedoeling is de technieken en verplaatsingen op een efficiënte manier te leren uitvoeren. Elke beweging moet met de nodige controle uitgevoerd worden. Op de eerste plaats komt het aspect "respect voor elkaar" naar voor, telkens moet er worden gegroet alvorens de oefeningen aan te vatten. Er bestaan verschillende vormen van Kumite training. Hier volgen de meest voorkomende met een korte beschrijving.</p>
  
    <h1>Enkele basis Kata's</h1>
    <table>
        <thead>
          <tr>
            <th class="w20">Type</th>
            <th>Beschrijving</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Gohon Kumite</td>
            <td>Dezelfde aanval wordt 5 x herhaald na elkaar door de "tori" of aanvaller.
                De "uke" of verdediger herhaald 5 maal dezelfde afweer en na de 5de maal plaatst deze een tegenaanval.
                Deze technieken moeten uitgevoerd worden met de nodige snelheid en kontrole.</td>
          </tr>
          <tr>
            <td>Sanbon Kumite </td>
            <td>In deze trainingsvorm wordt door "tori" 3 maal een aanval geplaatst, telkens een verschillende. "Uke" voert 3 afweren uit en plaatst op het einde een tegenaanval.
                Er bestaan 3 verschillende combinaties, uiteraard kan hierop verder gevarieerd worden.</td>
          </tr>
          <tr>
            <td>Kihon Ippon Kumite </td>
            <td>"Tori" vertrekt vanuit Zenkutsu-Dachi - Gedan-Barai.
                Er wordt een aanval aangekondigd en kort daarna uitgevoerd. "Uke" vertrekt vanuit Hachiji-Dachi of aandachtshouding. Wanneer de aanval geplaatst wordt, moet de verdediger deze afweren en een tegenaanval plaatsen.
                Uiteraard dienen alle techinieken wederom technisch en gecontroleerd te worden uitgevoerd.</td>
          </tr>
          <tr>
            <td>Kaeshi Ippon Kumite </td>
            <td>Hierbij is tijdens 1 enkele combinatie elke partner afwisselend "Tori" en "Uke".
                Partner 1 plaatst aanval en partner 2 weert af. Partner 2 plaatst op zijn beurt een aanval en nu wordt partner 1 verdediger; deze weert af en plaatst een definitieve tegenaanval.</td>
          </tr>
          <tr>
            <td>Jiyu Ippon Kumite </td>
            <td>Dit is bijna identiek aan Kihon Ippon Kumite, alleen dat nu beide partners vertrekken vanuit gevechtshouding.
                Dit is dus een vorm die dichter bij het vrij gevecht aanleunt.</td>
          </tr>
          <tr>
            <td>Okuri Jiyu Ippon Kumite </td>
            <td>Hier is de aanvaller "Tori" 2 x na elkaar aanvaller.
                De verdediger weert telkens af met tegenaanval.</td>
          </tr>
          <tr>
            <td>Happo Kumite </td>
            <td>Bij Happo Kumite is er 1 verdediger en zijn er 3 verschillende aanvallers die elk om beurt een aanval plaatsen.
                De verdediger weert elke anval af en plaatst telkens en tegenaanval.</td>
          </tr>
          <tr>
            <td>Jiyu Kumite</td>
            <td>Dit is het eigenlijke vrij gevecht.
                Alhoewel dit "vrij gevecht" genoemd wordt is het toch zeer strikt gereguleerd.
                De technieken moeten gecontroleerd uitgevoerd worden en er mogen geen open-hand-technieken gebruikt worden als aanval.
                De bedoeling is om punten te scoren en zo de wedstrijd te winnen.
                Het is vrij wie hier een willekeurig aanval plaatst, er worden geen afspraken gemaakt op voorhand.
                De tegenstander verrassen met snelle aanval of tegenaanval is het eigenlijke concept.</td>
          </tr>
        </tbody>
      </table>

  </div>
</template>

<style scoped>
.activityContainer {
  margin: 2rem 10rem;
  word-break: break-all;
  overflow-wrap: break-word;  
  hyphens: auto;  
}
h1 {
    text-align: center;
    font-weight: normal;
}
.flex {
    display: flex;
    justify-content: space-between;
}
table, th, td {
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-collapse: collapse;
}
table {
  width: 100%;
  -webkit-box-shadow: 3px 2px 4px 0px rgba(0,0,0,0.38);
  -moz-box-shadow: 3px 2px 4px 0px rgba(0,0,0,0.38);
  box-shadow: 3px 2px 4px 0px rgba(0,0,0,0.38);
  background-color: white;
  word-break: break-all;
  text-align: center;
}
td, th {
  white-space:normal;
  padding: 1rem;
  word-break: break-word;
}
.table__regelement, .inleiding {
    text-align: start;
    word-break: break-word;
}

h1 {
    margin-top: 5rem;
}
.w20 {
    width: 20%;
}

@media only screen and (max-width: 600px)  {
.activityContainer {
  margin: 2rem 0;
}
}
</style>
  
