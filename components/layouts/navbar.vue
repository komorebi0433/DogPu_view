<template>
  <el-row>
    <el-col :span="24">
      <div class="grid-content bg-purple-dark">
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
          <el-menu-item index="1">首页</el-menu-item>
          <el-menu-item index="2">联赛</el-menu-item>
          <el-menu-item index="3">杯赛</el-menu-item>
          <el-menu-item index="4">国家队</el-menu-item>
          <el-menu-item index="5">数据</el-menu-item>
          <el-submenu index="6">
            <template slot="title">我的工作台</template>
            <el-menu-item index="6-1">选项1</el-menu-item>
            <el-menu-item index="6-2">选项2</el-menu-item>
            <el-menu-item index="6-3">选项3</el-menu-item>
            <el-submenu index="6-4">
              <template slot="title">选项4</template>
              <el-menu-item index="6-4-1">选项1</el-menu-item>
              <el-menu-item index="6-4-2">选项2</el-menu-item>
              <el-menu-item index="6-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item><el-input v-model="input" placeholder="请输入内容" class="el-input"></el-input></el-menu-item>
          <el-menu-item index="11">
            <el-row class="demo-avatar demo-basic">
              <el-col :span="12">
                <div class="demo-basic--circle">
                  <div class="block"><el-avatar :size="45" :src="circleUrl"></el-avatar></div>
                </div>
              </el-col>
            </el-row>
          </el-menu-item>
          <el-menu-item index="7">
            <router-link to="/" tag="li" exact>
              <a>登录</a>
            </router-link>
          </el-menu-item>
          <el-menu-item index="8">注册</el-menu-item>
          <el-menu-item index="9">历史</el-menu-item>
          <el-menu-item index="10">收藏</el-menu-item>
        </el-menu>
      </div>
    </el-col>
    
  </el-row>
  
  <!-- <div class="line"></div> -->
  <!-- <el-menu
    :default-active="activeIndex2"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
    background-color="#545c64"
    text-color="#fff"
    active-text-color="#ffd04b">
    <el-menu-item index="1">处理中心</el-menu-item>
    <el-submenu index="2">
      <template slot="title">我的工作台</template>
      <el-menu-item index="2-1">选项1</el-menu-item>
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
    <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>
  </el-menu> -->
</template>

<script>
export default {
  name: 'navbar',

  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1',
      circleUrl: "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png",
      input: ''
    };
  },

  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style scoped>
.el-input {
  width: 400px;
}

.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}

.el-col {
  border-radius: 4px;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
</style>
