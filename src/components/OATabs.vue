<template>
  <div id="OATabs">
    <el-tabs type="card" :closable="true" @tab-click="handleClick" @tab-remove="handleRemove">
      <el-tab-pane label="个人主页" :closable="false" v-if="">
      <OAHome></OAHome>
      </el-tab-pane>
      <el-tab-pane v-for="data in tablist" :label="data.msg">
          <component v-bind:is="data.currentView" :tablist="tablist" >
          </component>
      </el-tab-pane>
  </div>
</template>

<script>
  import bus from '../bus'
  import OAHome from './component/OAHome'
  import AccessoriesManagement from './component/AccessoriesManagement'
  import RoleManagement from './component/RoleManagement'
  import TaskCompensation from './component/TaskCompensation'
  export default {
    name: 'OATabs',
    components: {
      OAHome,
      AccessoriesManagement,
      RoleManagement,
      TaskCompensation
    },
    methods: {
      handleRemove(tab) {
      },
      handleClick(tab, event) {
      }
    },
    created: function () {
      const vm = this
      bus.$on('openTab', function (tabName) {
        console.log('$on openTab', tabName)
        // TODO: 避免重复
        vm.$data.tablist.push({
          msg: tabName,
          currentView: 'RoleManagement'
        })
      })
    },
    data() {
      return {
        tablist: [
            {msg: '配置管理',currentView: 'RoleManagement'},
            {msg: '客户管理',currentView: 'AccessoriesManagement'},
            {msg: '定时任务补偿',currentView: 'TaskCompensation'}
        ]
      };
  },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
  .el-tabs {
    width: 100%;
  }
  .el-tabs__header {
    background-color:#3071b3;
    width: 100%;
  }
  .el-tabs__item {
    color: #fff;
  }
  .el-tabs__item.is-active {
    color: #3071B3;
    font-weight: bold;
  }
  .el-tabs--card .el-tabs__item.is-active {
    background-color: #fff;
    border-top-left-radius:5px;
    border-top-right-radius:5px;
  }
</style>
