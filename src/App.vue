<template>
  <v-app>
    <v-toolbar app class="px-5" dark color="#0d1321">
      <v-toolbar-title class="white--text kumbh">
        <span style="font-weight: 700">Covid</span> Tracker
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn
        v-on="on"
        color="#353c97"
        class="kumbh"
        @click="dialog.main = !dialog.main"
        >Como você está?</v-btn
      >

      <v-dialog v-model="dialog.main" max-width="450px">
        <v-card>
          <v-card-title>
            <v-spacer></v-spacer>
            <span class="headline justify-center" text-xs-center
              >Como você está se sentindo hoje?</span
            >
            <v-spacer></v-spacer>
          </v-card-title>
          <v-card-text>
            <v-container grid-list-md class="pt-0">
              <v-layout align-center justify-center row fill-height>
                <v-flex xs6 text-xs-center>
                  <v-btn large block color="success" style="font-weight: 700"
                    >Bem</v-btn
                  >
                </v-flex>
                <v-flex xs6 text-xs-center>
                  <v-btn
                    large
                    block
                    dark
                    color="error"
                    style="font-weight: 700"
                    @click="dialog.bad = !dialog.bad"
                    >Mal</v-btn
                  >
                </v-flex>
              </v-layout>
            </v-container>
          </v-card-text>
        </v-card>
      </v-dialog>

      <v-dialog v-model="dialog.bad" max-width="450px">
        <v-card>
          <v-card-title>
            <span class="headline">Como você está se sentindo hoje?</span>
          </v-card-title>
        </v-card>
      </v-dialog>

      <v-btn class="kumbh" flat>Tabela</v-btn>

      <v-btn class="kumbh" flat>Sobre</v-btn>

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
  data() {
    return {
      dialog: {
        main: false,
        bad: false,
      },
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@300;400;700&display=swap");

.kumbh {
  font-family: "Kumbh Sans";
}
</style>
