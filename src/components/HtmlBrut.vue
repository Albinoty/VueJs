<template>
    <div>
        <input type="text" v-model="valeur">
        <!-- Il est possible de faire une condtion ternaire pour afficher un contenu -->
        <p>{{valeur ? "Il y a quelque chose" : "Il n'y a rien"}}</p>
        <!-- Il est possible d'afficher du html en brut qui est stocké. -->
        <!-- on utilise v-html pour indiquer qu'on convertir en html -->
        <p v-html="HtmlBrut">{{HtmlBrut}}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            valeur: "",
            HtmlBrut: "<p>Je suis du HTML Brut</p>"
        }
    },

}
</script>