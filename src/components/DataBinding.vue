<template>
  <div>
    <h2>V-bind</h2>
    <!-- on assigne une donnée avec le v-bind -->
    <!-- le :href est l'attribut qu'on veut assigner -->
    <a v-bind:href="linkFb">Lien vers fb</a>
  </div>
</template>

<script>

export default {
  name: 'DataBinding',
  // C'est ici qu'on stock nos données
  data() {
    return {
      linkFb: 'https://facebook.com',
    }
  },
  // C'est la partie ou on déclare nos fonctions
  methods: {
   
  }
}
</script>
