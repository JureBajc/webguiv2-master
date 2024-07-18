<template>
    <v-container style="margin-right:40px">
      <v-expansion-panels class="custom-width" v-model="activePanels">
        <v-expansion-panel>
          <v-expansion-panel-title>DSP parameters</v-expansion-panel-title>
          <v-expansion-panel-text>
            <v-expansion-panels>

              <v-expansion-panel>
                <v-expansion-panel-title>Acquisition Parameters</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels>
                    
                    <v-expansion-panel>
                      <v-expansion-panel-title>Pre-trigger</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testtrigger
                      </v-expansion-panel-text>
                    </v-expansion-panel>
                    
                    <v-expansion-panel>
                      <v-expansion-panel-title>Holdoff</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                  </v-expansion-panels>
                </v-expansion-panel-text>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-title>Trigger settings</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels>
                    
                    <v-expansion-panel>
                      <v-expansion-panel-title>General trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testtrigger
                      </v-expansion-panel-text>
                    </v-expansion-panel>
                    
                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel I trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel II trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel VII trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel VIII trigger settings</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                  </v-expansion-panels>
                </v-expansion-panel-text>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-title>Calibration</v-expansion-panel-title>
                <v-expansion-panel-text>
                  <v-expansion-panels>
                    
                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel I</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel II</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel VII</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-title>Channel VIII</v-expansion-panel-title>
                      <v-expansion-panel-text>
                        testholdoff
                      </v-expansion-panel-text>
                    </v-expansion-panel>

                  </v-expansion-panels>
                </v-expansion-panel-text>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-title>Input coupling</v-expansion-panel-title>
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
                <v-expansion-panel-title>Accelerometer</v-expansion-panel-title>
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
  .v-expansion-panel-title {
    font-weight: bold;
    color: white;
    background-color: #12142a;
  }
  .custom-width {
    max-width: 600px;
    margin: auto;
  }
  </style>
  