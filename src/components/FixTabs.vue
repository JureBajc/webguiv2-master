// implementation of the settings and a search functionality to find them.
<template>
    <v-container style="margin-right:40px">
      <v-autocomplete
        append-icon="mdi-layers-search-outline"
        v-model="search"
        :items="items"
        label="Search settings"
        @update:search="openPanel"
      ></v-autocomplete>

      <v-expansion-panels class="custom-width" v-model="mainPanel">
        <v-expansion-panel>
          <v-expansion-panel-title>DSP parameters</v-expansion-panel-title>
          <v-expansion-panel-text>

            <v-expansion-panels v-model="subPanel2">
              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Acquisition Parameters</v-expansion-panel-title>
                <v-expansion-panel-text>

                  <v-expansion-panels v-model="subPanel3">  
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
                      <v-expansion-panel-title id="colorThr">Channel I trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel II trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel VII trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel VIII trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>
                  </v-expansion-panels>

                </v-expansion-panel-text>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Calibration</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels v-model="subPanel3">
                    
                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel I</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel II</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel VII</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title id="colorThr">Channel VIII</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                  </v-expansion-panels>
                </v-expansion-panel-text>
              </v-expansion-panel>

              <v-expansion-panel v-model="subPanel2">
                <v-expansion-panel-title id="colorSec">Input coupling</v-expansion-panel-title>
                <v-expansion-panel-text>
                  Cinputcoup
                </v-expansion-panel-text>
              </v-expansion-panel>
            </v-expansion-panels>

          </v-expansion-panel-text>
        </v-expansion-panel>
         
        <spacer></spacer>
        
        <v-expansion-panel>
          <v-expansion-panel-title>Platform info</v-expansion-panel-title>
          <v-expansion-panel-text>

            <v-expansion-panels v-model="subPanel2">
              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Accelerometer</v-expansion-panel-title>
                <v-expansion-panel-text>
                  accelltest
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
        "Pre-trigger",
        "Holdoff",
        "General trigger settings",
        "Channel I trigger setting",
        "Channel II trigger setting",
        "Channel VII trigger setting",
        "Channel VIII trigger setting",
        "Channel I",
        "Channel II",
        "Channel VII",
        "Channel VIII",
        "Input coupling",
        "Accelerometer"
      ],
      mainPanel: [0],
      subPanel2: [],
      subPanel3: []
    };
  },
  methods: {
    openPanel(item) {
      switch (item) {
        case "Pre-trigger":
          this.mainPanel = [0];
          this.subPanel2 = [0];
          this.subPanel3 = [0];
          break;
        case "Holdoff":
          this.mainPanel = [0];
          this.subPanel2 = [0];
          this.subPanel3 = [1];
          break;
        case "General trigger settings":
          this.mainPanel = [0];
          this.subPanel2 = [1];
          this.subPanel3 = [0];
          break;
        case "Channel I trigger setting":
          this.mainPanel = [0];
          this.subPanel2 = [1];
          this.subPanel3 = [1];
          break;
        case "Channel II trigger setting":
          this.mainPanel = [0];
          this.subPanel2 = [1];
          this.subPanel3 = [2];
          break;
        case "Channel VII trigger setting":
          this.mainPanel = [0];
          this.subPanel2 = [1];
          this.subPanel3 = [3];
          break;
        case "Channel VIII trigger setting":
          this.mainPanel = [0];
          this.subPanel2 = [1];
          this.subPanel3 = [4];
          break;
        case "Channel I":
          this.mainPanel = [0];
          this.subPanel2 = [2];
          this.subPanel3 = [0];
          break;
        case "Channel II":
          this.mainPanel = [0];
          this.subPanel2 = [2];
          this.subPanel3 = [1];
          break;
        case "Channel VII":
          this.mainPanel = [0];
          this.subPanel2 = [2];
          this.subPanel3 = [2];
          break;
        case "Channel VIII":
          this.mainPanel = [0];
          this.subPanel2 = [2];
          this.subPanel3 = [3];
          break;
        case "Input coupling":
          this.mainPanel = [0];
          this.subPanel2 = [3];
          this.subPanel3 = [];
          break;
        case "Accelerometer":
          this.mainPanel = [1];
          this.subPanel2 = [0];
          this.subPanel3 = [];
          break;
        default:
          this.mainPanel = [];
          this.subPanel2 = [];
          this.subPanel3 = [];
      }
    }
  }
};

</script>
  
  <style scoped>
  #colorThr{
    background-color:#0f93cd;
  }
  #colorSec{
    background-color:#1a5d7c;
  }
  .v-expansion-panel-title {
    font-weight: bold;
    color: white;
    background-color: #081d27;
  }
  .custom-width {
    max-width: 600px;
    margin: auto;
  }
  </style>
  