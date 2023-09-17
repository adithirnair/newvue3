<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <TemplateSyntaxExample/>
  <ReactivityFundamentals/>
  <ComputedProperties/>
  <ClassAndStyleBindings msg="MADE BY ADITHI"/>
  <EventHandling/>
  <FormInputBindings/>
  <WatchersOfVue/>
  <ChildComponents/>
  <ParentComponents/>
  <Home/>
  <About/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TemplateSyntaxExample from './components/TemplateSyntaxExample.vue';
import ReactivityFundamentals from  './components/ReactivityFundamentals.vue';
import ComputedProperties from './components/ComputedProperties.vue';
import ClassAndStyleBindings from './components/ClassAndStyleBindings.vue';
import EventHandling from './components/ClassAndStyleBindings.vue';
import FormInputBindings from './components/FormInputBindings.vue';
import WatchersOfVue from './components/WatchersOfVue.vue';
import ChildComponents from './components/ChildComponents.vue';
import ParentComponents from './components/ParentComponents.vue';
import Home from './components/Home.vue';
import About from './components/About.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TemplateSyntaxExample,
    ReactivityFundamentals,
    ComputedProperties,
    ClassAndStyleBindings,
    EventHandling,
    FormInputBindings,
    WatchersOfVue,
    ChildComponents,
    ParentComponents,
    Home,
    About


    
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
