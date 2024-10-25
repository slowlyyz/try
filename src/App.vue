<script setup lang="ts">
window.CESIUM_BASE_URL = "/Cesium"
import * as Cesium from "cesium"
import { onMounted } from "vue"
import "cesium/Build/Cesium/Widgets/widgets.css"


Cesium.Ion.defaultAccessToken = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiI5OGQxZDAzOC04YzFjLTQwNzMtOGZjMC0zMTRhYzY1N2FkNDAiLCJpZCI6ODMzNTgsImlhdCI6MTY0NTUzNjcyMX0.AREOCiP3UMdHDlvJsCfs0aMWtQqAUxVBWtNqRBLdCPE"

onMounted(() => {
    const viewer = new Cesium.Viewer("cesiumContainer", {
        terrain: Cesium.Terrain.fromWorldTerrain(),
    })
})

</script>

<template>
<div id="cesiumContainer"></div>
  
</template>

<style scoped>

</style>
