<template>
    <v-autocomplete
      v-model="selectedItem"
      :items="autocompleteItems"
      label="Select a panel"
      @change="onSelectionChange"
    ></v-autocomplete>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    name: 'ExpanAutocomplete',
    props: {
      items: {
        type: Array,
        required: true
      }
    },
    emits: ['select'],
    setup(props, { emit }) {
      const selectedItem = ref(null);
  
      const onSelectionChange = (value) => {
        emit('select', value);
      };
  
      return {
        selectedItem,
        autocompleteItems: props.items,
        onSelectionChange
      };
    }
  };
  </script>
  
  <style scoped>
  /* Add any scoped styles here */
  </style>
  