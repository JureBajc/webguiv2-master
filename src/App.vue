<template>
  <v-app>
        <v-app-bar elevation="0" color="#12142a" >
          <v-img style="margin-left:14px"
          src="../public/Logo_iTech_White_Horizontal_2.png"
          alt=""
          max-height="580px"
          max-width="200px"
          contain
          ></v-img>
          <v-toolbar-title style="margin-left:42px">
            X-Logger
          </v-toolbar-title>

          <v-icon icon="mdi-numeric-4-circle"></v-icon>
          <span>Quad, 12 bit | Sample rate: 160 Msps</span>
          <v-spacer></v-spacer>
          <v-img src="../public/Alstom.png" alt=""
          max-height="55px"
          max-width="110px"
          contain
          ></v-img>
          <v-spacer></v-spacer>
          <span>11:00PM</span>
          <v-icon icon="mdi-battery"></v-icon>
          <v-icon icon="mdi-connection"></v-icon>
          <v-icon style="margin-right:20px" icon="mdi-lan-connect"></v-icon>
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
    FixTabs,
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