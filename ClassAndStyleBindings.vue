<template>
    <div>
      <!-- Class Binding -->
      <div :class="getClassObject"></div>
  
      <!-- Style Binding -->
      <div :style="getStyleObject"></div>
    </div>
  </template>
  
  <script>
  import { ref, computed } from 'vue';
  
  export default {
    setup() {
      // Class Binding
      const isActive = ref(true);
      const hasError = ref(false);
  
      // Computed property to generate class object dynamically
      const getClassObject = computed(() => {
        return {
          active: isActive.value,
          error: hasError.value,
        };
      });
  
      // Style Binding
      const textColor = ref('blue');
      const textSize = ref(16);
  
      // Computed property to generate style object dynamically
      const getStyleObject = computed(() => {
        return {
          color: textColor.value,
          fontSize: textSize.value + 'px',
        };
      });
  
      return {
        isActive,
        hasError,
        textColor,
        textSize,
        getClassObject,
        getStyleObject,
      };
    },
  };
  </script>
  
  