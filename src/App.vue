<template>
  <v-app>
      <v-layout class="rounded-md">
        <v-app-bar elevation="0" color="#12142a" >
          <v-img src="../public/Logo_iTech_White_Horizontal_2.png" alt=""
          max-height="580px"
          max-width="200px"
          class="mb-1"
          contain
          ></v-img>
          <v-toolbar-title class="ml-2">
            X-Logger
          </v-toolbar-title>

          <v-icon icon="mdi-numeric-4-circle"></v-icon>
          <v-spacer></v-spacer>
          <v-img src="../public/Alstom.png" alt=""
          max-height="55px"
          max-width="110px"
          class="mb-1"
          contain
          ></v-img>
          <v-spacer></v-spacer>
          <v-icon icon="mdi-battery" class="ms-2"></v-icon>
          <v-icon icon="mdi-connection" class="ms-2"></v-icon>
          <v-icon icon="mdi-lan-connect" class="ms-2"></v-icon>
          <span class="ms-2">11:00PM</span>
          <v-spacer></v-spacer>
        </v-app-bar>

        <v-main>
          <GraphArea></GraphArea>

          <v-navigation-drawer v-bind:width="400" location="right">
            <DropMenu></DropMenu>
            <FixTabs></FixTabs>
          </v-navigation-drawer>

          <LeftSideMenu/>

          <FooterCenter/>

        </v-main>
      </v-layout>
  </v-app>
</template>

<script>
import DropMenu from './components/DropMenu.vue';
import GraphArea from './components/GraphArea.vue';
import LeftSideMenu from './components/LeftSideMenu.vue';
import FooterCenter from './components/FooterCenter.vue';
import FixTabs from './components/FixTabs.vue';
export default {
  name: 'App',

  components: {
    GraphArea,
    DropMenu,
    LeftSideMenu,
    FooterCenter,
    FixTabs
  }
}
</script> 
<style>
html {
  overflow: hidden !important;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

html::-webkit-scrollbar {
  width: 0;
  height: 0;
}
.center {
  text-align: center;
}
</style>