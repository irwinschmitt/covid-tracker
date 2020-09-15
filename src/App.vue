<template>
  <v-app>
    <v-toolbar app class="px-5" dark color="#0d1321">
      <v-toolbar-title class="white--text">
        <span style="font-weight: 700">Covid</span> Tracker
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn flat>Tabela</v-btn>

      <v-btn flat>Sobre</v-btn>

      <v-btn icon>
        <v-icon>search</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>refresh</v-icon>
      </v-btn>
    </v-toolbar>

    <v-content>
      <Map></Map>
    </v-content>
  </v-app>
</template>

<script>
import Map from "./components/Map";

export default {
  name: "App",
  components: {
    Map,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@300;400;700&display=swap");

.application {
  font-family: "Kumbh Sans";
}
</style>
