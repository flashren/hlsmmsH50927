<template>
    <el-aside width="230px">
      <!-- 左侧顶部的标题 -->
      <div id="leftTitle">
        <h1>华联超市管理系统</h1>
        <p>你好，Admin</p>
        <p>
          <router-link to="/">管理首页</router-link> |
          <a>退出系统</a>
        </p>
      </div>

      <!-- 左侧菜单 -->
      <el-menu
        :default-active="$route.path"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
        :unique-opened="isOpened"
      >
        <!-- 第1个菜单 -->
        <el-submenu index="1">
          <template slot="title">
            <span>账号管理</span>
          </template>
          <el-menu-item index="/useradd"><router-link to="/useradd">添加用户</router-link></el-menu-item>
          <el-menu-item index="/userlist"><router-link to="/userlist">管理用户</router-link></el-menu-item>
         <el-menu-item index="/pwdedit"><router-link to="/pwdedit">修改密码</router-link></el-menu-item>
        </el-submenu>
        

        <!-- 第2个菜单 -->
        <el-submenu index="2">
          <template slot="title">
            <span>导航2</span>
          </template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
          <el-menu-item index="1-3">选项2</el-menu-item>
        </el-submenu>

        <!-- 第3个菜单 -->
        <el-submenu index="3">
          <template slot="title">
            <span>导航3</span>
          </template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
          <el-menu-item index="1-3">选项2</el-menu-item>
        </el-submenu>

        <!-- 第4个菜单 -->
        <el-submenu index="4">
          <template slot="title">
            <span>导航4</span>
          </template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
          <el-menu-item index="1-3">选项2</el-menu-item>
        </el-submenu>
      </el-menu>
    </el-aside>
</template>

<script>
export default {
  data(){
     return {
         isOpened: true
     }
  },
  //菜单展开和收起的方法
  methods: {
    handleOpen(key, keyPath) {
      //console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      //console.log(key, keyPath);
    }
  }
}
</script>

<style>

</style>

