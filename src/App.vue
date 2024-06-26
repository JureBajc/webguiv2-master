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
          <DropMenu></DropMenu>
        </v-app-bar>

        <v-navigation-drawer>
          <v-list>
          <v-list-item title="Drawer left"></v-list-item>
          </v-list>
          </v-navigation-drawer>
    
        <v-navigation-drawer location="right">
          <v-list>
          <v-list-item style="border: 1px solid black;"><p>'Selected Device'</p></v-list-item>
          <v-list-item> <FixTabs></FixTabs></v-list-item>
          </v-list>
        </v-navigation-drawer>
    
        <v-main>
          <GraphArea></GraphArea>
        </v-main>
      </v-layout>
      <v-footer class="d-flex flex-column" style="text-align:center;" color="#12142a" app>
        <div class="center" align="center">
        <span class="white--text center" style="text-align: center;">&copy; Instrumentation Technologies - Jure Bajc 2024</span>
        </div>
      </v-footer>
  </v-app>
</template>

<script>
import DropMenu from './components/DropMenu.vue'
import FixTabs from '/src/components/FixTabs.vue'
import GraphArea from './components/GraphArea.vue';
export default {
  name: 'App',

  components: {
    GraphArea,
    DropMenu,
    FixTabs,
  },
  data: () => ({
      items: [
        { title: 'Device0' },
        { title: 'Device1' },
        { title: 'Device2' },
        { title: 'Device3' },
      ],
    }),
}
</script> 
<style>
html { overflow-y: auto }
.center {
  text-align: center;
}
</style>