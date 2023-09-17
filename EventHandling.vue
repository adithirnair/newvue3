<template>
    <button @click="handleClick">Click me</button>
  </template>
  
  <script>
  export default {
    setup() {
      const handleClick = () => {
        // Handle the click event
        console.log('Button clicked');
      };
  
      return {
        handleClick,
      };
    },
  };
  </script>
  
  