<template>
  <div class="process-step-table">
    <el-table :data="tableData" style="width: 100%">
      <el-table-column prop="testlocation" label="检测点" width="180"></el-table-column>
      <el-table-column prop="testcontent" label="检测内容" width="180"></el-table-column>
      <el-table-column prop="boundcondition" label="边界条件" width="180"></el-table-column>
      <el-table-column prop="pr" label="PR号" width="180"></el-table-column>
      <el-table-column prop="service" label="服务号(SID)" width="180"></el-table-column>
      <el-table-column prop="parameter" label="服务参数(ID)" width="180"></el-table-column>
      <el-table-column prop="value" label="值" width="180"></el-table-column>
      <el-table-column prop="timeout" label="超时时间" width="180"></el-table-column>
    </el-table>
  </div>
</template>
<script>
export default {
  name: 'ProcessStepTable',
  data () {
    return {
      tableData: [{
        testlocation: 'TEST_IB1',
        testcontent: 'TEST',
        boundcondition: 'TEST',
        pr: 'TEST',
        service: 'TEST',
        parameter: 'TEST',
        value: 'TEST',
        timeout: 'TEST'
      }]
    }
  }
}
</script>
<style>
  .process-step-table {
    display: flex;
    flex-grow: 1;
  }
</style>

