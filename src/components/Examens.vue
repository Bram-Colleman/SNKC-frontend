<script setup>
import { ref, onMounted, computed, reactive} from "vue";



const emit = defineEmits(["view"]);
let examens = ref([]);
let addView = ref(false);
let examen = reactive({
  datum: '',
  plaats: '',
  opmerking: '',
})

function getExamens() {
  fetch("https://snkc-backend.onrender.com/api/v1/examens/", {
    method: "GET",
    headers: {
      "content-type": "application/json",
    },
  })
  .then((response) => response.json())
  .then((data) => {
    console.log(data);
    examens.value = data.data.examens;
  })
  .catch((error) => {
    console.log(error);
  });
}

function setDateFormat(dateString) {
  let date = new Date(Date.parse(dateString));
  return date.toLocaleDateString('en-GB', {day: "numeric", month: "short", year: "numeric"});
}


onMounted(() => {
  getExamens();
})

</script>

<template>
  <div class="examenContainer">

  <div class="flex">
      <table>
        <thead>
          <tr>
            <th>Datum</th>
            <th>Plaats</th>
            <th>Opmerking</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="e in examens" :key="e.datum">
            <td>{{ setDateFormat(e.datum) }}</td>
            <td>{{ e.plaats }}</td>
            <td>{{ e.opmerking }}</td>
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
  
