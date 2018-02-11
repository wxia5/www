<template>
  <el-container>
    <el-header>
      <headMenu></headMenu>
    </el-header>
    <el-container>
      <el-aside width="150px">
        <leftMenu></leftMenu>
      </el-aside>
      <el-main>
        <router-view></router-view>
        <div id="cesiumContainer">
      </div>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
require('../node_modules/cesium/Source/Widgets/widgets.css');
let Cesium = require('../node_modules/cesium/Source/Cesium.js');
import headMenu from "./components/headMenu.vue"
import leftMenu from "./components/leftMenu.vue"

export default {
	components:{
		headMenu:headMenu,
		leftMenu:leftMenu
	},
  name: 'App',
  data(){
  	return {

  	}
  },
  mounted:function(){
  	var viewer = new Cesium.Viewer("cesiumContainer");
  	    viewer.camera.flyTo({
    destination : Cesium.Cartesian3.fromDegrees(-117.16, 32.71, 15000.0)
});
  }
}
</script>

<style>
body{
  margin: 0;
}

</style>
