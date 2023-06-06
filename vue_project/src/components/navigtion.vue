<template>
  <div>
    <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
    >
      <el-menu-item index="1">logo</el-menu-item>
      <el-menu-item index="2">首页</el-menu-item>
      <el-submenu index="3">
        <template slot="title">陪诊服务</template>
        <el-menu-item index="3-1">选项1</el-menu-item>
        <el-menu-item index="3-2">选项2</el-menu-item>
        <el-menu-item index="3-3">选项3</el-menu-item>
      </el-submenu>
      <el-submenu index="4">
        <template slot="title">住院陪诊</template>
        <el-menu-item index="4-1">选项1</el-menu-item>
        <el-menu-item index="4-2">选项2</el-menu-item>
        <el-menu-item index="4-3">选项3</el-menu-item>
      </el-submenu>
      <el-menu-item index="5">代办买药</el-menu-item>
      <el-menu-item index="6">急救小知识</el-menu-item>
    </el-menu>
    <div class="pos">
      <div class="search"><input type="text" placeholder="Ctrl+K" /></div>
      
      <div class="icon"><img src="../assets/tx.jpg" alt=""></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "navigtionView",
  data() {
    return {
      activeIndex: "2",
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style scoped>
.pos{
  float: right;
}
.search{
  margin-right:150px ;
  position: absolute;
  top: 20px;
  right: 50px;
  float: right;
}
.search input {
  width: 400px;
  height: 30px;
  padding: 0 10px;
  outline: none;
}
.pos div{
  display: inline-block;
}
.icon{
  position: absolute;
  top: 13px;
  right: 50px;
  background-color:red;
  width: 50px;
  height: 50px;
  border-radius: 7px;
  color: white;
  font-size: 15px;
  overflow: hidden;
}
.icon img{
  width: 100%;
}

</style>