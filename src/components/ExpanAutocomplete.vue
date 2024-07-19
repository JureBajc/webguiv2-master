<template>
    <v-container style="margin-right:40px">
      <v-autocomplete
        v-model="search"
        :items="items"
        label="Select a panel"
        @change="openPanel"
      ></v-autocomplete>

      <v-expansion-panels class="custom-width" v-model="activePanels">
        <v-expansion-panel>
          <v-expansion-panel-title>DSP parameters</v-expansion-panel-title>
          <v-expansion-panel-text>
            <v-expansion-panels v-model="subPanel1">
              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Acquisition Parameters</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels v-model="subPanel2">
                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Pre-trigger</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testtrigger
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Holdoff</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-expansion-panel-text>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Trigger settings</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels v-model="subPanel3">
                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">General trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testtrigger
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel I trigger setting</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testChannel I
                      </v-expansion-panel-text>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-expansion-panel-text>
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
      items: [
        "DSP parameters",
        "Acquisition Parameters",
        "Pre-trigger",
        "Holdoff",
        "Trigger settings",
        "General trigger settings",
        "Channel I trigger setting",
        "Channel II trigger setting",
        "Channel VII trigger setting",
        "Channel VIII trigger setting",
        "Calibration",
        "Channel I",
        "Channel II",
        "Channel VII",
        "Channel VIII",
        "Input coupling",
        "Platform info",
        "Accelerometer"
      ],
      activePanels: [],
      subPanel1: [],
      subPanel2: [],
      subPanel3: []
    };
  },
  methods: {
    openPanel(item) {
      switch (item) {
        case "DSP parameters":
          this.activePanels = [0];
          this.subPanel1 = [];
          this.subPanel2 = [];
          this.subPanel3 = [];
          break;
        case "Acquisition Parameters":
          this.activePanels = [0];
          this.subPanel1 = [0];
          this.subPanel2 = [];
          this.subPanel3 = [];
          break;
        case "Pre-trigger":
          this.activePanels = [0];
          this.subPanel1 = [0];
          this.subPanel2 = [0];
          this.subPanel3 = [];
          break;
        case "Holdoff":
          this.activePanels = [0];
          this.subPanel1 = [0];
          this.subPanel2 = [1];
          this.subPanel3 = [];
          break;
        case "Trigger settings":
          this.activePanels = [0];
          this.subPanel1 = [1];
          this.subPanel2 = [];
          this.subPanel3 = [];
          break;
        case "General trigger settings":
          this.activePanels = [0];
          this.subPanel1 = [1];
          this.subPanel2 = [];
          this.subPanel3 = [0];
          break;
        case "Channel I trigger setting":
          this.activePanels = [0];
          this.subPanel1 = [1];
          this.subPanel2 = [];
          this.subPanel3 = [1];
          break;
        default:
          this.activePanels = [];
          this.subPanel1 = [];
          this.subPanel2 = [];
          this.subPanel3 = [];
      }
    }
  }
};
</script>

<style>
/* Add any custom styles here */
</style>
