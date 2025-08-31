<template>
  <ol-map
    :loadTilesWhileAnimating="true"
    :loadTilesWhileInteracting="true"
    style="height: 400px"
  >
    <ol-view
      ref="view"
      :center="center"
      :zoom="zoom"
      :projection="projection"
    />

    <ol-tile-layer>
      <ol-source-osm />
    </ol-tile-layer>

    <ol-graticule-layer
      :show-labels="true"
      :wrap-x="false"
      :stroke-style="strokeStyle"
    >
    </ol-graticule-layer>
  </ol-map>
</template>

<script setup lang="ts">
import { Stroke } from "ol/style";
import { ref } from "vue";

const center = ref([0, 0]);
const projection = ref("EPSG:4326");
const zoom = ref(3);

const strokeStyle = new Stroke({
  color: "rgba(255,120,0,0.9)",
  width: 2,
  lineDash: [0.5, 4],
});
</script>
