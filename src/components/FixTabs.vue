<template>
    <v-container v-bind:width="400">
      <v-expansion-panels>
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
                  triggertest
                </v-expansion-panel-text>
              </v-expansion-panel>
              <v-expansion-panel>
                <v-expansion-panel-title>Calibration</v-expansion-panel-title>
                <v-expansion-panel-text>
                  calibtest
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
          <v-expansion-panel-title>Parent Panel 2</v-expansion-panel-title>
          <v-expansion-panel-text>
            <v-expansion-panels>
              <v-expansion-panel>
                <v-expansion-panel-title>Child Panel 2.1</v-expansion-panel-title>
                <v-expansion-panel-text>
                  Content for Child Panel 2.1
                </v-expansion-panel-text>
              </v-expansion-panel>
              <v-expansion-panel>
                <v-expansion-panel-title>Child Panel 2.2</v-expansion-panel-title>
                <v-expansion-panel-text>
                  Content for Child Panel 2.2
                </v-expansion-panel-text>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-expansion-panel-text>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </template>
  
  <script>

  </script>
  
  <style scoped>
  .v-expansion-panel-title {
    font-weight: bold;
  }
  </style>
  