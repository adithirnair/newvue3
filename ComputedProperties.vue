<template>
    <div>
      <p>Count: {{ count }}</p>
      <p>Doubled Count: {{ doubledCount }}</p>
      <p>Squared Count: {{ squaredCount }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { ref, computed } from 'vue';
  
  export default {
    setup() {
      const count = ref(0);
  
      // Computed properties
      const doubledCount = computed(() => count.value * 2);
  
      const squaredCount = computed(() => count.value * count.value);
  
      const increment = () => {
        count.value++;
      };
  
      return {
        count,
        doubledCount,
        squaredCount,
        increment,
      };
    },
  };
  </script>
  