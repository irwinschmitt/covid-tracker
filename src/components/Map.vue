<template>
  <div id="map" class="map"></div>
</template>

<script>
import axios from "axios";
import L from "leaflet";

export default {
  name: "Map",
  data() {
    return {
      map: null,
      tileLayer: null,
      cases: null,
    };
  },
  created() {
    this.getCases();
  },
  mounted() {
    this.$nextTick(() => {
      this.initMap();
    });
  },
  methods: {
    async getCases() {
      try {
        const response = await axios.get(
          "https://5f60d59a90cf8d00165586aa.mockapi.io/api/cases"
        );

        this.cases = response.data;
      } catch (error) {
        console.error(error);
      }
    },
    initMap() {
      this.map = L.map("map", {
        minZoom: 3,
        maxZoom: 16,
        zoomControl: false,
      }).setView([-15.793986, -47.882725], 12);

      L.control
        .zoom({
          position: "topright",
          zoomInTitle: "Aproximar",
          zoomOutTitle: "Distanciar",
        })
        .addTo(this.map);

      this.tileLayer = L.tileLayer(
        "https://api.mapbox.com/styles/v1/irwinschmitt/ckf3mx1qp0itv19plinr5jomv/tiles/256/{z}/{x}/{y}@2x?access_token=pk.eyJ1IjoiaXJ3aW5zY2htaXR0IiwiYSI6ImNrZW4xeDA1NjAwZjQyd21qZHRvZzVmeXUifQ.cTlT6Kio9SFYmmGfBj4oeg",
        {
          attribution:
            "© <a href='https://www.mapbox.com/about/maps/'>Mapbox</a> © <a href='http://www.openstreetmap.org/copyright'>OpenStreetMap</a> <strong><a href='https://www.mapbox.com/map-feedback/' target='_blank'>Improve this map</a></strong>",
        }
      ).addTo(this.map);
    },
  },
};
</script>

<style>
.map {
  height: 93.4vh;
}
</style>