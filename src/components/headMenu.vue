<template>
<div id="header">
<div class="line"></div>
<el-menu
  :default-active="activeIndex2"
  class="el-menu-demo"
  mode="horizontal"
  @select="handleSelect"
  background-color="#545c64"
  text-color="#fff"
  active-text-color="#ffd04b">
  <el-menu-item index="1" id="first-item">三维平台</el-menu-item>
  <el-submenu index="2">
    <template slot="title">地图切换</template>
    <el-menu-item index="2-1">卫星图</el-menu-item>
    <el-menu-item index="2-2">矢量图</el-menu-item>
  </el-submenu>
  <el-menu-item index="3"><a href="https://www.ele.me" target="_blank">模型加载</a></el-menu-item>
</el-menu>
</div>
</template>

<script>
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '3'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
      	console.log(key)
        console.log(keyPath);
      }
    }
  }
</script>
<style>
	#header{
		z-index: 999;
		/*position: absolute;*/
	}
	#first-item{
		width: 200px;
	}
</style>