<template>
  <div v-bind:width="400" fixed class="text-center">
    <v-select
      v-model="device"
      :items="devices"
      label="Device"
    ></v-select>
    <v-menu :device="device">
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
          <v-divider></v-divider>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
<script>
  export default {
    data: () => ({
      devices: [
        'Device0',
        'Device1',
        'Device2',
        'Device3',
        'Device4',
      ],
      device: 'Device0',
    }),
  }
</script>

<style>

</style>