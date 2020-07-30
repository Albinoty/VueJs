<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{ titre }}</h1>
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
    <!-- On ecoute l'event qui change titre, et on execute une fonction pour changer le titre -->
    <!-- En parametre, on recupere l'info recupérer dans l'enfant -->
    <Props v-bind:prenom="prenom" v-on:changeTitre="changementTitre($event)" />
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
      titre: "Vue",
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
    // En parametre l'info qui vient de l'enfant
    changementTitre: function(nvTitre){
      this.titre = nvTitre;
    }
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
