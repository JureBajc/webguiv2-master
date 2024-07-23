// This is a test component to demonstrate the use of v-autocomplete and v-expansion-panels
<template>
    <v-container>
      <v-autocomplete
        v-model="search"
        :items="items"
        label="Select a panel"
        @update:search="openPanel"
      ></v-autocomplete>
  
      <v-expansion-panels v-model="mainPanel">
        <v-expansion-panel>
          <v-expansion-panel-title>Platform info</v-expansion-panel-title>
          <v-expansion-panel-text>
            <v-expansion-panels v-model="subPanel">
              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec"
                  >Accelerometer</v-expansion-panel-title
                >
                <v-expansion-panel-text> accelltest </v-expansion-panel-text>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-expansion-panel-text>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        search: "",
        items: ["Platform info", "Accelerometer"],
        mainPanel: [],
        subPanel: []
      };
    },
    methods: {
      openPanel(item) {
        if (item === "Platform info") {
          this.mainPanel = [0];
          this.subPanel = [];
        } else if (item === "Accelerometer") {
          this.mainPanel = [0];
          this.subPanel = [0];
        }
      }
    }
  };
  </script>
  
  <style>
  /* Add any custom styles here */
  </style>
  