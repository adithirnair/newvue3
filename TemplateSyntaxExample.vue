<template>
    <!-- 1. Template Syntax -->
    <div>
      <!-- a. Text Interpolation -->
      <p>{{ message }}</p>
      
      <!-- b. Raw HTML [v-html] -->
      <div v-html="rawHtml"></div>
      
      <!-- c. Attribute Bindings [v-bind:id] -->
      <button :id="buttonId">Click me</button>
      
      <!-- d. JavaScript expressions inside syntax i.e.{{ }} -->
      <p>{{ 2 + 2 }}</p>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      // Data properties
      const message = ref('Hello, Vue 3');
      const rawHtml = ref('<span style="color: red;">Raw HTML</span>');
      const buttonId = 'my-button';
  
      return {
        message,
        rawHtml,
        buttonId,
      };
    },
  };
  </script>
 