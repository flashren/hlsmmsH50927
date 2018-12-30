<template>
  <el-container id="home">
    <!-- 左侧 -->
    <LeftMenu></LeftMenu>
    <!-- 右侧 -->
    <el-container id="mainContent">
      <!-- 顶部 -->
      <RightTop></RightTop>
      <!-- 中间 -->
      <el-main>
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <h3>密码修改</h3>
          </div>
          <div class="text item">
             <!-- 模板的内容 -->
          </div>
        </el-card>
      </el-main>
      <!-- 底部 -->
      <RightBottom></RightBottom>
    </el-container>
  </el-container>
</template>

<script>
//引入导航组件
import LeftMenu from '../components/leftMenu';
import RightTop from '../components/rightTop';
import RightBottom from '../components/rightBottom';

export default {
  data() {
    return {
      
    };
  },
  components: {
    //注册组件
    LeftMenu,
    RightTop,
    RightBottom
  }
};
</script>


<style>
/* scoped 作用域限定样式只在当前组件生效 */
</style>













