<template>
    <div>
      <!-- a. v-for with an Object -->
      <ul>
        <li v-for="(value, key) in myObject" :key="key">{{ key }}: {{ value }}</li>
      </ul>
  
      <!-- b. v-for with a Range -->
      <ul>
        <li v-for="n in 5" :key="n">{{ n }}</li>
      </ul>
  
      <template>
  <div>
    <template v-for="item in items" :key="item.id">
      <div>{{ item.name }}</div>
      <hr />
    </template>
  </div>
      </template>

  
      <!-- d. v-for with v-if -->
      <ul>
        <li v-for="item in items" :key="item.id" v-if="item.active">{{ item.name }}</li>
      </ul>
  
      <!-- e. v-for with a Component -->
      <ul>
        <custom-item
          v-for="item in items"
          :key="item.id"
          :item="item"
          @custom-event="handleCustomEvent"
        ></custom-item>
      </ul>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const myObject = ref({ a: 1, b: 2, c: 3 });
      const items = ref([
        { id: 1, name: 'Item 1', active: true },
        { id: 2, name: 'Item 2', active: false },
        { id: 3, name: 'Item 3', active: true },
      ]);
  
      const handleCustomEvent = (data) => {
        // Handle custom event from child component
      };
  
      return {
        myObject,
        items,
        handleCustomEvent,
      };
    },
  };
  </script>
  