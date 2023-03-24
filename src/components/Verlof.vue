<script setup>
</script>

<template>
  <div class="examenContainer">

  <div class="flex">
      <table>
        <thead>
          <tr>
            <th></th>
            <th>Begindatum</th>
            <th>Einddatum</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Paaszondag</td>
            <td>09 Apr 2023</td>
            <td>09 Apr 2023</td>
          </tr>
          <tr>
            <td>Hemelvaart</td>
            <td>18 May 2023</td>
            <td>18 May 2023</td>
          </tr>
          <tr>
            <td>Pinksteren</td>
            <td>28 May 2023</td>
            <td>28 May 2023</td>
          </tr>
          <tr>
            <td>Zomervakantie</td>
            <td>01 Jul 2023</td>
            <td>31 Aug 2023</td>
          </tr>
          <tr>
            <td>Allerzielen</td>
            <td>02 Nov 2023</td>
            <td>02 Nov 2023</td>
          </tr>
          <tr>
            <td>Wapenstilstand</td>
            <td>11 Nov 2023</td>
            <td>11 Nov 2023</td>
          </tr>
          <tr>
            <td>Kerstvakantie</td>
            <td>22 Dec 2023</td>
            <td>05 Jan 2024</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

</template>

<style scoped>
.flex {
  display: flex;
  flex-direction: column;
}
button {
  align-self: flex-end;
  margin: 1rem;
}
.examenContainer {
  margin: 2rem 10rem;
  word-break: break-all;
  overflow-wrap: break-word;  
  hyphens: auto;  
}

thead {
  color: #232323!important;
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

.t10 {
  width: 10%;
}
.t25 {
  width: 25%;
}
.t5 {
  width: 5%;
}

@media only screen and (max-width: 600px)  {
.examenContainer {
  margin: 2rem 0;
}
}
</style>
  
