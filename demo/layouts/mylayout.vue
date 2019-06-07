<template>
  <el-container >
    <el-header style="background-color:#545c64;">
      <!--nuxt-link to="/">Head</nuxt-link-->
      <el-menu default-active="1" class="el-menu-demo" mode="horizontal"       
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
          <el-menu-item index="1"><i class="el-icon-location"></i><span>处理中心</span></el-menu-item>
          <el-submenu index="2">
            <template slot="title">我的工作台</template>
            <el-menu-item index="2-1"><nuxt-link to="/">返回首页</nuxt-link></el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
              <template slot="title">选项4</template>
              <el-menu-item index="2-4-1">选项1</el-menu-item>
              <el-menu-item index="2-4-2">选项2</el-menu-item>
              <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="3" disabled>消息中心</el-menu-item>
          <el-menu-item index="4"><nuxt-link to="/">首页</nuxt-link></el-menu-item>
      </el-menu>
    </el-header>
    <el-container>
    <el-aside style="width:250px;background-color:#545c64;"> 
      <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
   
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>导航一</span>
        </template>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <template slot="title">选项4</template>
          <el-menu-item index="1-4-1">选项1</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="2">
        <i class="el-icon-menu"></i>
        <span slot="title">导航二</span>
      </el-menu-item>
      <el-menu-item index="3" disabled>
        <i class="el-icon-document"></i>
        <span slot="title">导航三</span>
      </el-menu-item>
      <el-menu-item index="4">
        <i class="el-icon-setting"></i>
        <span slot="title">导航四</span>
      </el-menu-item>
    </el-menu>
    </el-aside>
      <el-main>
          <nuxt/>
      </el-main>
    </el-container>
  </el-container>
</template>
<script>
export default {
  name: 'pos',
  mounted: function () {
    //原生获取屏幕高度
    //var orderHight = $(window).height();
    //console.log('323'+orderHight);
    $('.el-aside').height(parseInt($(window).height())-parseInt($('.el-header').height()));
    //document.getElementById('order-list').style.height = orderHight + 'px'
  }
}
</script>
<style>


  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
  }
a{
 text-decoration:none;  /*超链接无下划线*/
}
a:visited{
  color:#ccc;

}
</style>
