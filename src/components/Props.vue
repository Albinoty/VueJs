<template>
    <!-- On appel la propriété qui est prenom -->
    <h2>Coucou {{prenom}}</h2>
</template>
<script>
export default {
    data(){

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