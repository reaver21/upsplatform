<template>
  <div class="app">
    <AppHeader></AppHeader> 
    <div class="main-body">
      <div class="body-left">
        <el-button type='success'>默认按钮</el-button> 
      </div>
      <div class="body-content">   
        <ProcessStepTable></ProcessStepTable>
      </div>
    </div>
  </div>
</template>

<script>
  import AppHeader from './MainPage/AppHeader.vue'
  import MainSideMenu from './MainPage/MainSideMenu.vue'
  import ProcessStepTable from './TextModels/ProcessStepTable.vue'

  export default {
    name: 'MainPage',
    components: {
      AppHeader, MainSideMenu, ProcessStepTable
    }
  }
</script>

<style scope>
  body {
    display: block;
    margin: 0;
  }
  header {
  }
  html {
  background-color: white;
  font-size: 16px;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  min-width: 300px;
  overflow-x: hidden;
  overflow-y: hidden;
  text-rendering: optimizeLegibility;
  -webkit-text-size-adjust: 100%;
     -moz-text-size-adjust: 100%;
      -ms-text-size-adjust: 100%;
          text-size-adjust: 100%;
  } 
  .app {
    display: flex;
    flex-direction: column;
    height: 100vh;
  }
  .main-body {
    display: flex;
    flex-direction: row;
    flex-grow: 1;
  }
  .body-left {
    display: flex;
    flex-direction: column;
    width: 200px;
    padding: 5px 10px;
  }
  .body-content {
    display: flex;
    flex-grow: 1;
    border-left: 1px solid #ddd;
    overflow-x: auto;
  }
</style>
