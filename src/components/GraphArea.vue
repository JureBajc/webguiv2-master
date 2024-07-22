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
      >
        <v-btn>Add Graph</v-btn>
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
  },
}
</script>