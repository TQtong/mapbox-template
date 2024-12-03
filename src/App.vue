<script setup lang="ts">
import { onMounted } from 'vue'
import mapboxgl from 'mapbox-gl'

onMounted(() => {
  mapboxgl.accessToken = 'YOUR_MAPBOX_ACCESS_TOKEN'
  const map = new mapboxgl.Map({
    container: 'map', // container ID
    style: 'mapbox://styles/mapbox/streets-v12', // style URL
    center: [-74.5, 40], // starting position [lng, lat]
    zoom: 9 // starting zoom
  })

  console.log(map)
})
</script>

<template>
  <div id="container">
    <div id="map"></div>
  </div>
</template>

<style scoped lang="scss">
#container {
  width: 100%;
  height: 100%;

  #map {
    width: 100%;
    height: 100%;
  }
}
</style>
