<script setup>
import { ref } from 'vue'

import Activities from './components/Activities.vue'
import ActivitiesShort from './components/ActivitiesShort.vue'
import Examens from './components/Examens.vue'
import Nav from './components/Nav.vue'
import Footer from './components/Footer.vue'
import About from './components/About.vue'
import Kata from './components/Kata.vue'
import Kumite from './components/Kumite.vue'
import Contact from './components/Contact.vue'
import Verlof from './components/Verlof.vue'

let view = ref("home");

function changeView(string) {
  view.value = string;
}
</script>

<template>  

  <div class="container">
    <Nav @view="changeView"></Nav>
    <h1 v-if="view == 'home'">Aankomende activiteiten</h1>
    <ActivitiesShort @view="changeView" v-if="view == 'home'"></ActivitiesShort>

    <h1 v-if="view == 'actueel'">Actueel</h1>
    <Activities @view="changeView" v-if="view == 'actueel'"></Activities>
    <h1 v-if="view == 'actueel'">Examens</h1>
    <Examens @view="changeView" v-if="view == 'actueel'"></Examens>
    <h1 v-if="view == 'actueel'">Verlofperiodes</h1>
    <Verlof @view="changeView" v-if="view == 'actueel'"></Verlof>
    <About @view="changeView" v-if="view == 'overons'"></About>
    <Kata @view="changeView" v-if="view == 'kata'"></Kata>
    <Kumite @view="changeView" v-if="view == 'kumite'"></Kumite>
    <Contact @view="changeView" v-if="view == 'contact'"></Contact>

    <Footer @view="changeView"></Footer>
  </div>

</template>

<style scoped>
.container {
  /* background-color: rgb(222, 222, 222); */
  background-color: white;
  width: 98%;
  margin: 1rem 1rem 0 1rem;
  position: absolute;
  top: 0;
  left: 0;
  overflow-x: hidden;
  z-index: -1;
}

.demo-tabs > .el-tabs__content {
  
  padding: 32px;
  color: #6b778c;
  font-size: 32px;
  font-weight: 600;
}
.el-tabs {
  margin: 1rem;
}

.container h1 {
  text-align: center;
  font-weight: normal;
}



</style>
