<template>
  <div>
    <h2>V-bind</h2>
    <a v-bind:href="linkFb">Lien vers fb</a>
  </div>
</template>

<script>


export default {
  name: 'DataBinding',
  data() {
    return {
      linkFb: 'https://facebook.com',
    }
  },
  components: {
    
  },
  methods: {
   
  }
}
</script>
