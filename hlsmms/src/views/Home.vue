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
            <h3>系统信息</h3>
          </div>
          <div class="text item">
            <el-alert title="成功提示的文案" type="success" show-icon></el-alert>
            <el-alert title="消息提示的文案" type="info" show-icon></el-alert>
            <!-- 一行两列 -->
            <el-row :gutter="40">
              <!-- 左侧 -->
              <el-col :span="12">
                <el-card class="box-card">
                  <div slot="header" class="clearfix">
                    <h3>销售排行</h3>
                  </div>
                  <div class="text item">
                    <el-table :data="tableData" stripe style="width: 100%">
                      <el-table-column prop="goodsname" label="商品名称"></el-table-column>
                      <el-table-column prop="salenum" label="销量"></el-table-column>
                    </el-table>
                  </div>
                </el-card>
              </el-col>
              <!-- 右侧 -->
              <el-col :span="12">
                <el-card class="box-card">
                  <div slot="header" class="clearfix">
                    <h3>缺货商品</h3>
                  </div>
                  <div class="text item">
                    <el-table :data="tableData" stripe style="width: 100%">
                      <el-table-column prop="goodsname" label="商品名称"></el-table-column>
                      <el-table-column prop="salenum" label="销量"></el-table-column>
                    </el-table>
                  </div>
                </el-card>
              </el-col>
            </el-row>
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
      tableData:[
        {goodsname: "测试商品1", salenum: 20},
        {goodsname: "测试商品2", salenum: 10},
        {goodsname: "测试商品3", salenum: 20},
        {goodsname: "测试商品4", salenum: 30},
        {goodsname: "测试商品5", salenum: 50}
      ]
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













