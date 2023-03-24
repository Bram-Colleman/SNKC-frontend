<script setup>

</script>

<template>
  <div class="activityContainer">
    <h1>Contact</h1>
    <div class="flex">
        <div>
              <h1>Email</h1>
              <a href="mailto: snkc.karate@gmail.com">snkc.karate@gmail.com</a>
        </div>
        <div>
              <h1>Telefoon</h1>
              <a href="tel:0473863637">0473 86 36 37</a>
        </div>
        <div>
              <h1>Facebook</h1>
              <a href="https://www.facebook.com/groups/15661517571" target="_blank">Sint-Niklase Karateclub</a>
        </div>
    </div>


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
    justify-content: space-evenly;
    text-align: center;
}
.flex div {
    width: 25%;
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

a {
    color: rgb(67, 67, 67);
}
</style>
  
