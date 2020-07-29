<template>
    <div>
        <button v-on:click="compteurA++">+1</button>
        <button v-on:click="compteurA--">-1</button>
        <h2>CompteurA: {{compteurA}}</h2>
        <p>{{checkValeur()}}</p>
    </div>
</template>
<script>
export default {
    data() {
        return {
            compteurA: 0,
            compteurB: 0
        }
    },
    methods: {
        checkValeur: function (){
            console.log("La fonction s'est lancée");

            return this.compteurA > 10 ? "Supérieur à 10" : "Inférieur à 10"
        }
    },
    // Watch permet de surveiller une propriétée
    watch: {
        // Pour agir dans la propriétée il faudra l'appel par son nom
        // Suivi d'une function
        compteurA: function(){
            //Ici, nous allons remettre à zero apres 2 secondes.
            // Fonction Fléchée
            setTimeout(() => {
                this.compteurA = 0
            }, 2000);
            // Attention, on declare une fonction classique
            // Il va créer un nouveau scoop 
            // Il faudra une variable passer le this dans la fonction
            // let scoop = this;
            // setTimeout(function () {
            //     scoop.compteurA = 0
            // }, 2000);
        }
    },
    computed: {
        memo: function () {
            console.log("Memo s'est lancée");

            return this.compteurA > 10 ? "Supérieur à 10" : "Inférieur à 10"
        }
    }
}
</script>