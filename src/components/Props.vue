<template>
    <div>
        <!-- On appel la propriété qui est prenom -->
        <h2>Coucou {{prenom}}</h2>
        <button v-on:click="changeTitre">Changer le titre</button>
    </div>
</template>
<script>
export default {
    data(){
        return {

        }
    },
    methods: {
        changeTitre: function (){
            // Emit permet de créer un event que le parent peut ecouter
            // 1) nom de l'evnement
            // 2) ce qu'on veut passer
            this.$emit('changeTitre','J\'ai changé le titre')
        }
    },
    // on declare le props ici
    // props: ['prenom']
    // il est possible d'ajouter une validation au props
    props: {
        prenom: {
            // Définit le type du props
            type: String,
            // S'il est requis ou non
            required: true
        }
    }
}
</script>