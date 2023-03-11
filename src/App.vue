<script lang="ts" setup>
import Form from './components/Form.vue'
import Activities from './components/Activities.vue'

import { ref } from 'vue'
import type { TabsPaneContext } from 'element-plus'

const activeName = ref('Home')

const handleClick = (tab: TabsPaneContext, event: Event) => {
  console.log(tab, event)
}

</script>

<template>
  <el-tabs
    v-model="activeName"
    type="card"
    class="demo-tabs"
    @tab-click="handleClick"
  >
    <el-tab-pane label="Home" name="Home">Home</el-tab-pane>
    <el-tab-pane label="Actueel" name="Actueel"><Activities></Activities></el-tab-pane>
    <el-tab-pane label="test" name="second">Config</el-tab-pane>

  </el-tabs>


  <div class="container">
  </div>
</template>

<style scoped>
.container {
  background-color: rgb(222, 222, 222);
  height: 100vw;
  width: 98%;
  margin: 1rem 1rem 0 1rem;
  position: fixed;
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

</style>
