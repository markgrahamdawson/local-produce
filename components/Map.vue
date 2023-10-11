<template>
    <div id="map" />
  </template>
  
  <script setup lang="ts">
  import mapboxgl from "mapbox-gl";
  import "mapbox-gl/dist/mapbox-gl.css";
  import { onMounted } from "vue";

  onMounted(() => {
    const runtimeConfig = useRuntimeConfig()
    console.log(runtimeConfig.public.mapKey)
    mapboxgl.accessToken = runtimeConfig.public.mapKey
    const map = new mapboxgl.Map({
      container: "map",
      style: "mapbox://styles/mapbox/light-v9",
      zoom: 10,
      center: [-5.5376, 50.1188]
    });
    map.on('load', () => {
    // TODO: Here we want to load a layer
    // TODO: Here we want to load/setup the popup
    });
  });

  </script>
  
  <style>
  #map {
    height: 100vh;
  }
  </style>