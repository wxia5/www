<template>
  <div id="app">
  	<headMenu></headMenu>
  	<leftMenu></leftMenu>
  	<cesiumMap></cesiumMap>
  </div>
  
</template>

<script>
require('../node_modules/cesium/Source/Widgets/widgets.css');
let Cesium = require('../node_modules/cesium/Source/Cesium.js');
import headMenu from "./components/headMenu.vue"
import leftMenu from "./components/leftMenu.vue"
import cesiumMap from "./components/cesiumMap.vue"

export default {
	components:{
		headMenu:headMenu,
		leftMenu:leftMenu,
		cesiumMap:cesiumMap
	},
  name: 'App',
  data(){
  	return {
  		
  	}
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
