<script setup>

</script>

<template>
  <div class="activityContainer">
    <h1>Kata</h1>
    <p class="inleiding">Een kata is een ingebeeld gevecht tegen 7, 8 of meerdere tegenstanders die van alle richtingen aanvallen uit voeren. Deze denkbeeldige aanvallen worden afgeweerd en de aanvallers worden uitgeschakeld of de moed ontnomen om verder aan te vallen. Deze kata's hebben een vaste vorm of mal die per stijl kan verschillen, nochtans is de basis dezelfde. Van deze mal kan wat betreft standen, richtingen, technieken en zelfs timing niet worden afgeweken. Dit maakt het extra moeilijk om deze kata's perfect uit te voeren. Enkel met optimale kontrole, concentratie en inzet kan men een goed resultaat bekomen. EEN KATA WORDT NIET NAGEDAAN MAAR "BELEEFD". Er bestaan 26 verschillende "kata's" in Shotokan Karate. Hiervan zijn er 15 basis kata's die Funakoshi naar Japan bracht in 1922, hieraan gaf hij bepaalde kenmerken. Hierna volgt een beknopt overzicht.</p>
  
    <h1>Enkele basis Kata's</h1>
    <table>
        <thead>
          <tr>
            <th>Kata</th>
            <th>Technieken</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Heian Shodan </td>
            <td>voorwaartse en achterwaartse stand, voetbeweging en voorwaartse stoot</td>
          </tr>
          <tr>
            <td>Heian Nidan </td>
            <td>voorwaartse en zijwaartse trap terwijl men van richting verandert</td>
          </tr>
          <tr>
            <td>Heian Sandan </td>
            <td>de verbinding met het lichaam tijdens het blokkeren met de onderarm. Slag met de achterkant van de vuist</td>
          </tr>
          <tr>
            <td>Heian Yondan </td>
            <td>variatie in technieken met de vereiste balans</td>
          </tr>
          <tr>
            <td>Heian Godan </td>
            <td>balans, evenwicht en sprong</td>
          </tr>
          <tr>
            <td>Tekki Shodan </td>
            <td>paardrijstand met heupbewegingen</td>
          </tr>
          <tr>
            <td>Tekki Nidan </td>
            <td>pakkende en hakkende bewegingen</td>
          </tr>
          <tr>
            <td>Tekki Sandan </td>
            <td>snel opeenvolgende technieken en blokkeringen op middenrifniveau</td>
          </tr>
          <tr>
            <td>Bassai-Dai </td>
            <td>voordeel halen uit benadeling door het gebruik van wisselende blokkeringen en het in verschillende mate toepassen van kracht</td>
          </tr>
          <tr>
            <td>Kanku-Dai </td>
            <td>variatie in snelle en langzame technieken. Springen</td>
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

@media only screen and (max-width: 600px)  {
.activityContainer {
  margin: 2rem 0;
}
}
</style>
  
