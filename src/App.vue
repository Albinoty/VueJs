<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Vue</h1>
    <!-- <DataBinding /> 
    <Event />
    <EventModifiers /> -->
    <!-- <KeyModifiers /> -->
    <VModel />
  </div>
</template>

<script>

// import DataBinding from './components/DataBinding.vue';
// import Event from './components/Event.vue';
// import EventModifiers from './components/EventModifiers.vue';
// import KeyModifiers from './components/KeyModifiers.vue';
import VModel from './components/VModel.vue';

export default {
  name: 'App',
  //On fait appel a des méthodes
  components: {
    // DataBinding,
    // Event,
    // EventModifiers,
    // KeyModifiers,
    VModel
  },
  // C'est la partie ou on déclare nos fonctions
  methods: {
   
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
