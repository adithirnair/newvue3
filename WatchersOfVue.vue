<template>
    <div>
      <input type="text" v-model="textToWatch" />
    </div>
  </template>
  
  <script>
  import { ref, watch } from 'vue';
  
  export default {
    setup() {
      // Data property to watch
      const textToWatch = ref('');
  
      // Watcher
      watch(textToWatch, (newValue, oldValue) => {
        console.log(`Text changed from "${oldValue}" to "${newValue}"`);
      });
  
      return {
        textToWatch,
      };
    },
  };
  </script>
  