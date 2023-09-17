<template>
    <div>
      <child-component :title="childTitle" @custom-event="handleChildEvent">
        <p>Slot content goes here</p>
      </child-component>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponents.vue';
  
  export default {
    components: {
      ChildComponent,
    },
    setup() {
      const childTitle = 'Child Component Title';
  
      const handleChildEvent = (data) => {
        console.log(`Received event from child component with data: ${data}`);
      };
  
      return {
        childTitle,
        handleChildEvent,
      };
    },
  };
  </script>
  