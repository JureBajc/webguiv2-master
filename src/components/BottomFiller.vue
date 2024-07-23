<template>
    <div class="container">
        <div class="box">
            {{ logMessage }}
        </div>
        <div class="box">
          <v-container>
            <v-row justify-content: space-evenly no-gutters>
                <v-col cols="8" class="boxp">
                  <v-sheet class="pa-2 ma-2">
                    RMS | Min | Max table - Device0
                  </v-sheet>
                </v-col>
                <v-col cols="4" class="boxp">
                  <v-sheet class="pa-2 ma-2">
                    <p>
                    AUX Signal - Device0
                    </p>
                      <ul>
                        <li>Voltage Input 0 [V]: 0.026</li>
                        <li>Voltage Input 1 [V]: 0.005</li>
                        <li>Voltage Input 2 [V]: 0.003</li>
                        <li>Voltage Input 3 [V]: 0.002</li>
                      </ul>
                  </v-sheet>
                </v-col>
              </v-row>
            </v-container>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            logMessage: ''
        }
    },
    created() {
        const originalConsoleLog = console.log;
        console.log = (...args) => {
            this.logMessage = 'Console: ' + args.join(' ');
            originalConsoleLog.apply(console, args);
        };
    }
}
</script>

<style>
.container {
    display: flex;
}
.bordert{
    border: 1px solid black;
}

.box {
    flex: 1;
    height: 200px;
    background-color: #f3f2f2;
    margin: 16px;
    display: flex;
    justify-content: start;
    align-items: start;
    font-size: 16px;
    word-wrap: break-word;
}
.boxp {
    width: 50%;
    height: 50%;
    border: 1px solid black;

}
ul li {
  background: #cce5ff;
  color: darkblue;
  margin: 5px;

}
</style>
