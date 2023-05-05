<template>
  <q-page>
    <div style="height: calc(100vh)">
      <GMapMap :center="center" :zoom="10" map-type-id="terrain">
        <GMapCluster :zoomOnClick="true">
          <GMapMarker
            :key="index"
            v-for="(m, index) in markers"
            :position="m.position"
            :clickable="true"
            :draggable="true"
            @click="center = m.position"
          />
        </GMapCluster>
      </GMapMap>
    </div>
  </q-page>
</template>

<script setup>
const center = { lat: 51.093048, lng: 6.84212 };
const markers = [
  {
    position: {
      lat: 51.093048,
      lng: 6.84212,
    },
  },
  {
    position: {
      lat: 51.198429,
      lng: 6.69529,
    },
  },
  {
    position: {
      lat: 51.165218,
      lng: 7.067116,
    },
  },
  {
    position: {
      lat: 51.09256,
      lng: 6.84074,
    },
  },
];
</script>
