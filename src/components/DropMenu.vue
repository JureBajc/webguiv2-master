<template>
    <div class="text-center">
        <v-menu
          open-on-click
        >
          <template v-slot:activator="{ props }">
            <v-btn
              class="dropbtn"
              bg-color="#12142a"
              color="white"
              v-bind="props"
            >
              Dropdown
            </v-btn>
          </template>
    
          <v-list>
            <v-list-item
              v-for="(item, index) in items"
              :key="index"
            >
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>

</template>
<script>
  export default {
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
  .dropbtn{
    margin-right: 20px;
  }
</style>