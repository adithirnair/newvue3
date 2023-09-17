<template>
    <div>
      <!-- a. v-model with various input types -->
      <input type="text" v-model="textInput" />
      <input type="checkbox" v-model="checkboxValue" />
      <input type="radio" v-model="radioValue" :value="1" />
      <input type="radio" v-model="radioValue" :value="2" />
      <select v-model="selectedOption">
        <option value="option1">Option 1</option>
        <option value="option2">Option 2</option>
      </select>
      <textarea v-model="textareaValue"></textarea>
  
      <!-- b. v-model modifiers -->
      <input type="text" v-model.lazy="lazyInput" />
      <input type="text" v-model.number="numericInput" />
      <input type="text" v-model.trim="trimmedInput" />
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      // Data properties
      const textInput = ref('');
      const checkboxValue = ref(false);
      const radioValue = ref(1);
      const selectedOption = ref('option1');
      const textareaValue = ref('');
  
      const lazyInput = ref('');
      const numericInput = ref(0);
      const trimmedInput = ref('');
  
      return {
        textInput,
        checkboxValue,
        radioValue,
        selectedOption,
        textareaValue,
        lazyInput,
        numericInput,
        trimmedInput,
      };
    },
  };
  </script>
  