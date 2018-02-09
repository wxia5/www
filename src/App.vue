<template>
  <div id="app">
  	<headMenu></headMenu>
  	<leftMenu></leftMenu>
		<div id="cesiumContainer">
		</div>
  </div>
  
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
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#cesiumContainer{
	height: 700px;
}
</style>
