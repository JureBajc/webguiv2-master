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
    <v-switch
    label="Pause graph"
    color="primary"
    
    >
    </v-switch>
  </v-container>
</template>

<style>
.container {
  margin: 10px 10px 10px 10px;
  padding: 0px 0px 0px 0px;
}
</style>
<script>
import SelectorMenu from './SelectorMenu.vue'

export default {
  components: {
    SelectorMenu
  },
  data: () => ({
  })
}
</script>