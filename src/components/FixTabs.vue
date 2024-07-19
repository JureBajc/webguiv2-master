<template>
    <v-container style="margin-right:40px">
      <v-expansion-panels class="custom-width" v-model="activePanels">
        <v-expansion-panel>
          <v-expansion-panel-title>DSP parameters</v-expansion-panel-title>
          <v-expansion-panel-text>
            <v-expansion-panels>

              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Acquisition Parameters</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels>
                    
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
                  <v-expansion-panels>
                    
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
                  <v-expansion-panels>
                    
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

              <v-expansion-panel>
                <v-expansion-panel-title id="colorSec">Input coupling</v-expansion-panel-title>
                <v-expansion-panel-text>
                  Cinputcoup
                </v-expansion-panel-text>
              </v-expansion-panel>

            </v-expansion-panels>
          </v-expansion-panel-text>
        </v-expansion-panel>
  
        <v-expansion-panel>
          <v-expansion-panel-title>Platform info</v-expansion-panel-title>
          <v-expansion-panel-text>

            <v-expansion-panels>
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
      activePanels: [0]
    };
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
  