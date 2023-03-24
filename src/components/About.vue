<script setup>
import Card from './Card.vue'


</script>

<template>
  <div class="activityContainer">
    <h1>Onze Club</h1>
    <div class="flex">
        <Card role="VOORZITTER / HOOFDLESGEVER / SENSEI"
              name="PAUL COLLEMAN"
              belt="2e Dan Shotokan"
              cert="Gediplomeerd Bloso lesgever"
              image="./src/assets/paul.jpeg"
        ></Card>
        <Card role="BESTUURSLID / LESGEVER / SEMPAI"
              name="TOM TERSAGO"
              belt="3e Dan Shotokan"
              cert='Gediplomeerd Bloso lesgever "initiatie"'
              image="./src/assets/tom.png"
        ></Card>
        <Card role="SECRETARIS"
              name="JOHAN CLAES"
              belt="2e Dan Shotokan"
              cert=""
              image="./src/assets/johan.png"
        ></Card>
    </div>
    <h1>Trainingen</h1>
    <p>Note: In juli is er <b>geen training</b> en in augustus <b>enkel donderdag</b> in sporthal "Witte molen" Sint Niklaas.</p>
    <table>
        <thead>
          <tr>
            <th>Dag</th>
            <th>Uur</th>
            <th>Plaats</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Dinsdag (vanaf blauwe gordel)</td>
            <td>19:00 - 20:00</td>
            <td>Temsica, Temse</td>
          </tr>
          <tr>
            <td>Donderdag</td>
            <td>19:00 - 20:30</td>
            <td>De kouter, Belsele</td>
          </tr>
          <tr>
            <td>Zaterdag</td>
            <td>10:30 - 12:00</td>
            <td>De witte molen, Sint-Niklaas</td>
          </tr>
          <tr>
            <td>Zondag</td>
            <td>10:30 - 12:00</td>
            <td>De kouter, Belsele</td>
          </tr>
        </tbody>
      </table>

    <h1>Examens</h1>
    <p>Van 1ste kyu naar 1ste dan (zwarte gordel), wordt 1 jaar gerekend vanaf doorgave aan de federatie van het behalen van de 1ste kyu.
        Klik hier om onze examenprogramma's bekijken.</p>
    <table>
        <thead>
          <tr>
            <th>Gordel</th>
            <th>Kyu</th>
            <th>Aantal lessen</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Wit (starter)</td>
            <td>9e kyu</td>
            <td></td>
          </tr>
          <tr>
            <td>Wit met zwart streepje</td>
            <td>8e kyu</td>
            <td>20</td>
          </tr>
          <tr>
            <td>Geel</td>
            <td>7e kyu</td>
            <td>30</td>
          </tr>
          <tr>
            <td>Oranje</td>
            <td>6e kyu</td>
            <td>40</td>
          </tr>
          <tr>
            <td>Groen</td>
            <td>5e kyu</td>
            <td>50</td>
          </tr>
          <tr>
            <td>Blauw</td>
            <td>4e kyu</td>
            <td>50</td>
          </tr>
          <tr>
            <td>Bruin</td>
            <td>3e kyu</td>
            <td>60</td>
          </tr>
          <tr>
            <td>Bruin met 1 streepje</td>
            <td>2e kyu</td>
            <td>80</td>
          </tr>
          <tr>
            <td>Bruin met 2 streepjes</td>
            <td>1e kyu</td>
            <td>100</td>
          </tr>
        </tbody>
    </table>

    <h1>Regelement</h1>
    <table class="table__regelement">
        <tbody>
          <tr>
            <td>1. Wees steeds tijdig aanwezig op de training.</td>
          </tr>
          <tr>
            <td>2. Gelieve de dojo NIET te betreden met schoenen.</td>
          </tr>
          <tr>
            <td>3. Steeds groeten bij het betreden van de dojo.</td>
          </tr>
          <tr>
            <td>4. Indien de les reeds bezig is eerst de dojo groeten en daarna de Sensei. Pas daarna mag U de groep vervoegen.</td>
          </tr>
          <tr>
            <td>5. Indien U de les vroegtijdig moet verlaten dient dit op voorhand aan de Sensei gemeld worden.</td>
          </tr>
          <tr>
            <td>6. De dojo mag tijdens de les niet verlaten worden zonder toestemming te vragen aan de Sensei.</td>
          </tr>
          <tr>
            <td>7. Vanaf men de dojo betreedt wordt de leraar aangesproken met "Sensei" (meester of leraar).</td>
          </tr>
          <tr>
            <td>8. Verwijder voor de training alle sierraden zoals uurwerken, ringen, kettingen enz.. Ook kauwgom of andere snoep is niet toegelaten. Vergeet niet na de training uw spullen mee te nemen.</td>
          </tr>
          <tr>
            <td>9. De club is niet verantwoordelijk voor verloren of verdwenen goederen, steek waardevolle spullen in uw sporttas en plaats deze aan de zijkant in de zaal, dit op een plaats die niet storend is tijdens de training.</td>
          </tr>
          <tr>
            <td>10. Tijdens de les wordt aan iedereen de volle inzet en concentratie gevraagd.</td>
          </tr>
          <tr>
            <td>11. Bij oefeningen met partner moet men steeds respect voor elkaar hebben. Het is niet toegelaten andere karateka's te bekritiseren of uit te lachen.</td>
          </tr>
          <tr>
            <td>12. Iedere karateka moet zichzelf voldoende verzorgen, lichaamshygiëne is zeer belangrijk.</td>
          </tr>
          <tr>
            <td>13. Voeten en handen dienen steeds goed gewassen te zijn.</td>
          </tr>
          <tr>
            <td>14. De nagels van vingers en tenen moeten kort geknipt zijn.</td>
          </tr>
          <tr>
            <td>15. De haren moeten verzorgd zijn en lang haar moet op een paardestaart gedragen worden of met een haarband vastgelegd worden.</td>
          </tr>
          <tr>
            <td>16. Na de training is het aan te raden om te douchen.</td>
          </tr>
          <tr>
            <td>17. Elke karateka moet een kimono (karate-gi) dragen zoals voorgeschreven, witte broek en dito vest met aangepaste gordel (OBI). Dit ten laatste 1 maand na aansluiting. Deze kledij kan eventueel aangekocht worden via de club.</td>
          </tr>
          <tr>
            <td>18. Een aangesloten lid moet steeds in orde zijn met de verzekering. Kontroleer dit voor uzelf, niet in orde is niet trainen!</td>
          </tr>
          <tr>
            <td>19. De club of lesgever is niet aansprakelijk voor ongevallen, zeker niet voor leden die niet in orde zijn met de verzekering.</td>
          </tr>
          <tr>
            <td>20. Het dragen van een bril tijdens de lessen is niet toegelaten, tenzij een aangepaste sportbril (onbreekbaar).</td>
          </tr>
          <tr>
            <td>21. Bij gebruik van materialen of toestellen wordt verwacht hiervoor zorg te dragen en deze na gebruik terug te plaatsen. Elke beschadiging moet onmiddellijk gemeld te worden aan de verantwoordelijke.</td>
          </tr>
          <tr>
            <td>22. Houdt u steeds aan de regels van goed gedrag en zeden.
                verzorg uw taalgebruik en toon respect voor anderen.
                Schep buiten de dojo niet op over uw kunde en gebruik deze niet buiten de dojo (tenzij in noodgevallen), een vermeden gevecht is steeds een gewonnen gevecht!!</td>
          </tr>
          <tr>
            <td>23. Inbreuken tegen de regels kunnen gesanktioneerd worden, dit kan gaan van schorsing tot uitsluiting. Van het betaalde verzekering lidgeld of aansluitingsgeld kan niets teruggevorderd worden.</td>
          </tr>
          <tr>
            <td>24. Bij het verlaten van de dojo steeds zorgen dat alle douches afgesloten zijn en de lichten gedoofd.</td>
          </tr>
          <tr>
            <td>25. Per jaar zijn er steeds 3 of 4 examens voorzien. Elk lid moet hiervoor de nodige trainingen gevolgd hebben. De kanditatuur kan geweigerd worden als de Sensei vindt dat het duidelijk nog te vroeg is.</td>
          </tr>
          <tr>
            <td>26.Indien tijdens de les een karateka moet pompen wegens sanktie opgelegd door de Sensei, moet dit steeds zonder morren of commentaar gedaan worden. Discipline is een hoofdbestanddeel om een goede karateka te worden.</td>
          </tr>
        </tbody>
      </table>

      <h1>Privacybeleid</h1>
      <p class="privacybeleid">Alle persoonlijke gegevens door de clubleden verschaft bij inschrijving worden enkel gebruikt binnen de club en op vraag van onze Federatie: Vlaamse Karate Federatie (VKF). Deze gegevens worden niet doorgegeven of verstuurd, noch per post noch per mail. In geen geval worden persoonlijke gegevens doorgegeven voor "directe of indirecte marketing". Elk lid heeft recht op inzage en correctie van eigen gegevens. Voor vragen of opmerkingen kunt u zich steeds wenden tot het bestuur van de club.</p>
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
.table__regelement, .privacybeleid {
    text-align: start;
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
  
