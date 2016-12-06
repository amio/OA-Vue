<template>
  <div id="OAHome">
    <el-row>
      <el-col :span="16">
        <div class="workParty">
          <div class="workParty-title work-icon" >
            我的工作
          </div>
          <div class="workParty-center" id="myWorkBody" >
            <div class="div-mywork" v-for="data in work" v-on:click="move(data.msg)">{{data.msg}}</div>
          </div>
        </div>
      </el-col>
      <el-col :span="8">
        <div class="workParty">
          <div class="workParty-title appDown-icon" >
            APP下载
          </div>
          <div class="workParty-center" id="appDownBody" >
            <span>OA-APP</span>
            <br/>
            <img src="../../assets/oacrm.png" alt=""/>
            <br/>
            <span>OA app仅支持安卓手机，用于设备管理、日常办公等</span>
            <br/>
            <span>审核APP</span>
            <br/>
            <img src="../../assets/qrcode.png" alt=""/>
            <br/>
            <span>审核 app仅支持安卓手机，用于商务条件审核、用款申请审核等，下载后请联系IT配置手机权限</span>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'OAHome',
  data() {
    return {
        work: [
            {msg: '用款申请'},
            {msg: '管理用款'}
                ]
      };  
  },
    methods: {
                move: function (src) {
                    console.log(tabdata)
                }
            }
  }  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/*工作组样式*/
.workParty{
    min-height:200px;
}
.workParty-title{
    width: 92%;
    border-bottom: 1px solid #CCCCCC;
    height: 49px;
    line-height: 49px;
    margin: 0 auto;
    font-size: 16px;
    color: #3071b3;
    background-repeat: no-repeat;
    background-position: left center;
    text-indent: 20px;
}
.work-icon{
    background-image: url(../../assets/icon_title1.gif);
}
.appDown-icon{
    background-image: url(../../assets/icon_title3.gif);
}
.workParty-center{
    width: 92%;
    height: 100%;
    margin: 0 auto;
    text-align: center;
    overflow: auto;
}
.div-mywork {
    width: 109px;
    height: 16px;
    float: left;
    font-size: 14px;
    color: #009AD5;
    margin-top: 14px;
    border-right: 1px solid #CCCCCC;
    text-align: center;
    cursor: pointer;
}
</style>
