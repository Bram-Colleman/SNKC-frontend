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
  fetch("http://localhost:3001/api/v1/activiteiten/", {
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

function addActivity() {
  let data = {
  titel: activity.titel,
  plaats: activity.plaats,
  datum: activity.datum,
  tijd: activity.tijd,
  opmerking: activity.opmerking
};
  fetch ("http://localhost:3001/api/v1/activiteiten", {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify(data),
  })
  .then((response) => response.json())
  .then((data) => {
    if(data.status == "Success") {
      getActivities();
      addView = false;
    }
  })
  .catch((error) => {
    console.log("Something went wrong");
  })
}

function setDateFormat(dateString) {
  let date = new Date(Date.parse(dateString));
  return date.toLocaleDateString('en-GB');
}


onMounted(() => {
  getActivities();
})

</script>

<template>
  <div class="activityContainer">

  <div class="flex">
      <el-button type="danger" @click="addView= !addView">Nieuwe activiteit</el-button>
      
  <div v-if="addView">
    <el-form :model="activity" label-width="120px" class="form">
      <el-form-item label="Titel">
        <el-input v-model="activity.titel" />
      </el-form-item>
      <el-form-item label="Plaats">
        <el-input v-model="activity.plaats" />
      </el-form-item>
      <el-form-item label="Tijdstip">
        <el-col :span="3">
          <el-date-picker v-model="activity.datum" type="date" placeholder="Datum" style="width: 100%"/>
        </el-col>
        <el-col :span="1" class="text-center">
          <span class="text-gray-500"></span>
        </el-col>
        <el-col :span="3">
          <el-time-select v-model="activity.tijd" start="00:00" step="00:15" end="23:59" placeholder="Uur" format="HH:mm"/>
        </el-col>
      </el-form-item>
      <el-form-item label="Opmerking">
        <el-input v-model="activity.opmerking" type="textarea"/>
      </el-form-item>
      <el-form-item>
        <el-button type="danger" @click="addActivity">Bevestig</el-button>
      </el-form-item>
    </el-form>
  </div>
  
      <table>
        <thead>
          <tr>
            <th class="t25">Titel</th>
            <th class="t10">Datum</th>
            <th>Opmerking</th>
            <th class="t10">Plaats</th>
            <th class="t5">Uur</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="a in activities" :key="a.titel">
            <td>{{ a.titel }}</td>
            <td>{{ setDateFormat(a.datum) }}</td>
            <td>{{ a.opmerking }}</td>
            <td>{{ a.plaats }}</td>
            <td>{{ a.uur }}</td>
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
  color: red!important;
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
  
