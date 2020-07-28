<template>
    <div>
        <p>Ton Nom</p>
        <!-- V-model va lier ce qu'on va ecrire dans l'input vers la valeur qu'on attribuer  -->
        <!-- data-binding -->
        <input type="text" v-model="valeur">
        <p>{{valeur}}</p>
    </div>
</template>

<script>
export default {
    data(){
        return{
            valeur: ""
        }
    },
    methods: {
        
    }
}
</script>