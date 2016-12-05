<template>
  <div id="OANavMenu">
    <div class="grid-content bg-purple-dark"></div>
    <div class="grid-content bg-purple-green"></div>
    <el-menu mode="vertical" default-active="1" class="el-menu-vertical-demo">
      <el-submenu index="1">
        <template slot="title">邮件管理</template>
        <el-menu-item index="1-1">写邮件</el-menu-item>
        <el-menu-item index="1-2">收件箱</el-menu-item>
        <el-menu-item index="1-3">已发邮件</el-menu-item>
        <el-menu-item index="1-4">草稿箱</el-menu-item>
        <el-menu-item index="1-5">报告收件人配置</el-menu-item>
      </el-submenu>
      <el-submenu index="2">
        <template slot="title">客户管理系统</template>
        <el-menu-item index="2-1">选项1</el-menu-item>
        <el-menu-item index="2-2">选项2</el-menu-item>
        <el-menu-item index="2-3">选项3</el-menu-item>
      </el-submenu>
      <el-submenu index="3">
        <template slot="title">重要事项跟踪</template>
        <el-menu-item index="3-1">选项1</el-menu-item>
        <el-menu-item index="3-2">选项2</el-menu-item>
        <el-menu-item index="3-3">选项3</el-menu-item>
      </el-submenu>
      <el-submenu index="4">
        <template slot="title">消息中心</template>
        <el-menu-item index="4-1">选项1</el-menu-item>
        <el-menu-item index="4-2">选项2</el-menu-item>
        <el-menu-item index="4-3">选项3</el-menu-item>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script>
  export default {
    name: 'OANavMenu'
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .el-menu {
    border-right: 1px solid #ddd;
    border-right: 1px solid #ddd;
  }
  .el-menu-item-group__title {
    height: 30px;
    line-height: 30px;
    color: White;
    padding-left: 0px;
    background-color: #3071b3;
    font-size: 12px;
  }
  .el-submenu__title {
    height: 30px;
    line-height: 30px;
    color: White;
    padding: 0px;
    background-color: #3071b3;
    text-align: center;
  }
 .el-submenu__title:hover {
    background-color: #3071b3;
  }
  .el-submenu__icon-arrow {
    position: absolute;
    top: 50%;
    right: 20px;
    margin-top: -7px;
    transition: transform .3s;
    display: none;
  }
  .el-submenu .el-menu-item {
    height: 30px;
    line-height: 30px;
    padding: 0;
    text-align: center;
    background-color: White;
    border-bottom: 1px solid #ddd;
    font-size: 12px;  }
  .el-menu-item, .el-submenu__title {
    font-size: 12px;
  }
</style>
