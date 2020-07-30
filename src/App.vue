<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Vue</h1>
    <!-- <DataBinding /> 
    <Event />
    <EventModifiers /> -->
    <!-- <KeyModifiers /> -->
    <!-- <VModel />, -->
    <!-- <HtmlBrut /> -->
    <!-- <Computed /> -->
    <!-- <Watch /> -->
    <!-- <ToggleCss /> -->
    <!-- <Condition /> -->
    <!-- <Boucle /> -->
    <!-- On passe une donnée à l'enfant -->
    <Props prenom="Albi" />
    <!-- Dynamiquement via les données de notre composant -->
    <Props v-bind:prenom="prenom" />
  </div>
</template>

<script>

// import DataBinding from './components/DataBinding.vue';
// import Event from './components/Event.vue';
// import EventModifiers from './components/EventModifiers.vue';
// import KeyModifiers from './components/KeyModifiers.vue';
// import VModel from './components/VModel.vue';
// import HtmlBrut from './components/HtmlBrut.vue';
// import Computed from './components/Computed.vue';
// import Watch from './components/Watch.vue';
// import ToggleCss from './components/ToggleCss.vue';
// import Condition from './components/Condition.vue';
// import Boucle from './components/Boucle.vue';
import Props from './components/Props.vue';


export default {
  name: 'App',
  data(){
    return {
      prenom: "Albinot"
    }
  },
  //On fait appel a des méthodes
  components: {
    // DataBinding,
    // Event,
    // EventModifiers,
    // KeyModifiers,
    // VModel,
    // HtmlBrut,
    // Computed,
    // Watch,
    // ToggleCss,
    // Condition,
    // Boucle,
    Props
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
