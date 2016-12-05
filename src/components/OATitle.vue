<template>
  <div id="OATitle">
    <el-button type="text">退出</el-button>
    <el-button type="text">进入网站</el-button>
  </div>
</template>

<script>
export default {
  name: 'OATitle'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #OATitle{
    height:30px;
    overflow: hidden;
    background-color:#3071b3;
  }
  #OATitle button{
    float:right;
    margin:0 10px;
    color:#a7d1fc;
  }
</style>
