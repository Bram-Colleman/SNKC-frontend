<script setup>
import { ref, onMounted, computed, reactive} from "vue";



const emit = defineEmits(["view"]);
let activities = ref([]);
let addView = ref(false);
let activity = reactive({
  titel: '',
  plaats: '',
  datum: '',
  tijd: '',
  opmerking: ''
})

function getActivities() {
  fetch("https://snkc-backend.onrender.com/api/v1/activiteiten/", {
    method: "GET",
    headers: {
      "content-type": "application/json",
    },
  })
  .then((response) => response.json())
  .then((data) => {
    activities.value = data.data.activiteiten;
  })
  .catch((error) => {
    console.log(error);
  });
}

function setDateFormat(dateString) {
  let date = new Date(Date.parse(dateString));
  return date.toLocaleDateString('en-GB',  {day: "numeric", month: "short", year: "numeric"});
}


onMounted(() => {
  getActivities();
})

</script>

<template>
  <div class="activityContainer">

  <div class="flex">
      <table>
        <thead>
          <tr>
            <th>Titel</th>
            <th>Datum</th>

          </tr>
        </thead>
        <tbody>
          <tr v-for="a in activities" :key="a.titel">
            <td>{{ a.titel }}</td>
            <td>{{ setDateFormat(a.datum) }}</td>
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
.activityContainer {
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
.activityContainer {
  margin: 2rem 0;
}
}
</style>
  
