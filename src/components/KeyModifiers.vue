<template>
    <div>
        <p>Ton Nom</p>
        <!-- On ecoute l'event de type keyup -->
        <!--le .enter permet de lancer la fonction si on appuie sur la touche enter -->
        <!-- il existe plusieurs touches possibles -->
        <!-- https://vuejs.org/v2/guide/events.html#Event-Modifiers -->
        <input type="text" v-on:keyup.enter="inputFunction">
    </div>
</template>

<script>
export default {
    methods: {
        inputFunction: function() {
            console.log("Tu as appuyé sur une touche")
        }
    }
}
</script>