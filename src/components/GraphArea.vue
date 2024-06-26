<template>
    <v-container style="background-color:#ECEFF1">
        <SelectorMenu></SelectorMenu>
      <v-row no-gutters>
        <v-col cols="6">
          <v-sheet class="pa-2">
            <v-img src="../../public/aux1.png" height="200px"></v-img>
          </v-sheet>
        </v-col>
        <v-col cols="6">
            <v-sheet class="pa-2">
                <v-img src="../../public/aux2.png" height="200px"></v-img>
            </v-sheet>
          </v-col>
        </v-row>
        <v-row no-gutters>
        <v-col cols="12">
          <v-sheet class="pa-2">
            <v-img src="../../public/aux3.png"></v-img>
          </v-sheet>
        </v-col>
      </v-row>
    </v-container>
  </template>


<style>

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