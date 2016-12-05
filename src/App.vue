<template>
  <div id="app">
    <OATitle></OATitle>
    <el-row>
      <el-col :span="2">
        <OANavMenu></OANavMenu>
      </el-col>
      <el-col :span="22">
        <OATabs></OATabs>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import OATitle from './components/OATitle'
import OANavMenu from './components/OANavMenu'
import OATabs from './components/OATabs'
export default {
  name: 'app',
  components: {
    OATitle,
    OANavMenu,
    OATabs
  }
}
</script>

<style>
  *{
    margin:0;
    padding:0;
  }
  .el-row {
    margin-bottom: 20px;

  }
  .grid-content {
    border-radius: 0px;
    min-height: 40px;
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #3071b3;
  }
  .bg-purple-green{
    min-height: 10px;
    background-color: #6CCE41;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }

  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>
