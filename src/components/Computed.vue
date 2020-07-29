<template>
    <div>
        <button v-on:click="compteurA++">+1</button>
        <button v-on:click="compteurA--">-1</button>
        <h2>CompteurA: {{compteurA}}</h2>
        <p>{{checkValeur()}}</p>
        <button v-on:click="compteurB++">+1</button>
        <button v-on:click="compteurB--">-1</button>
        <h2>CompteurB: {{compteurB}}</h2>
        <p>{{memo}}</p>
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
    // Le Computed agit comme une fonction mais il permet de faire tous ce qui est par rapport au valeur calculé
    // Contrairement au fonction, il n'a pas besoin de faire un re-render
    computed: {
        memo: function () {
            console.log("Memo s'est lancée");

            return this.compteurA > 10 ? "Supérieur à 10" : "Inférieur à 10"
        }
    }
}
</script>