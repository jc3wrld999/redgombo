<template>
  <card class="card-map" title="지진 발생지 예측" >
    <div class="map">
      <div id="map">


        <l-map style="width:100%; height: 100%" :zoom="zoom" :center="center">
      <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    </l-map>

      </div>
    </div>
  </card>
</template>
<script>
import "leaflet";
import "leaflet/dist/leaflet.css";

import { LMap, LTileLayer, LMarker } from "vue2-leaflet";

export default {
  name: "Map",
  components: { LMap, LTileLayer, LMarker },
  data: function() {
    return {
      zoom: 12,
      center: [51.505, -0.09],
      url: "http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
      attribution:
        '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    };
  }
};
</script>
<style></style>
