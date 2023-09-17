<template>
    <div>
      <h2>{{ title }}</h2>
      <button @click="emitEvent">Emit Event</button>
      <slot></slot>
    </div>
  </template>
  
  <script>
  import { defineProps, defineEmits } from 'vue';
  
  export default {
    props: {
      title: String,
    },
    setup() {
      // Define props to access them in the setup function
      const props = defineProps(['title']);
  
      // Emit custom event
      const emit = defineEmits();
  
      const emitEvent = () => {
        emit('custom-event', 'Data from child component');
      };
  
      return {
        props, // Make props accessible in the setup function
        emitEvent,
      };
    },
  };
  </script>
  