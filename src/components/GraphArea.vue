// This is the main component that will hold the graph and the buttons to interact with it, buttons lack functionality for now.
<template>
  <v-container fixed style="background-color:#ECEFF1">
    <SelectorMenu></SelectorMenu>
    <v-row no-gutters>
      <v-col cols="12">
        <v-sheet class="pa-2">
          <v-img src="../../public/aux3.png"></v-img>
        </v-sheet>
      </v-col>
    </v-row>
    <v-row no-gutters align="center">
      <v-btn-toggle
        v-model="toggle"
        variant="outlined"
        divided
        density="compact"
      >
        <v-btn @click="logTest">Add Graph</v-btn>
        <v-btn>Remove Graph</v-btn>
        <v-btn>Download Graph</v-btn>
        <v-btn :class="{ 'pause-active': isPaused }" @click="togglePause" class="default-green">Pause Graph</v-btn>
      </v-btn-toggle>
    </v-row>
  </v-container>
</template>

<style>
.container {
  padding: 0px 0px 0px 0px;
}
.default-green {
  background-color: #C8E6C9; /* Default green color */
}
.pause-active {
  background-color: #FFCDD2; /* Red color when active */
}
.scrollable {
  overflow-y: scroll;
}
</style>

<script>
import SelectorMenu from './SelectorMenu.vue'

export default {
  components: {
    SelectorMenu
  },
  data() {
    return {
      toggle: null,
      isPaused: false,
    };
  },
  methods: {
    togglePause() {
      this.isPaused = !this.isPaused;
    },
    logTest() {
      console.log("Uncaught TypeError: Cannot read property 'length' of undefined at Array.prototype.map (<anonymous>) at fetchData (app.js:45) at Object.callback (main.js:32) at handleResponse (ajax.js:67) at XMLHttpRequest.xhr.onreadystatechange (ajax.js:22)");
    },
  },
}
</script>