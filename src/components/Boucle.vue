<template>
    <div>
        <!-- boucle for -->
        <p v-for="element in 5" :key="element">Coucou {{element}}</p>
        <!-- Boucle d'un tableau de nombre -->
        <ul>
            <li v-for="nombre in tableau" :key="nombre">{{nombre}}</li>
        </ul>
        <!-- Boucle d'un table de String -->
        <ul>
            <li v-for="(fruit, index) in tableauFruit" :key="index">{{fruit}}</li>
        </ul>
        <!-- Boucle d'un objet en parcourant ses propriété -->
        <ul>
            <li v-for="(voiture, props) in objetVoiture" :key="props">{{props}} : {{voiture}}</li>
        </ul>
        <!-- Boucle d'un tableau d'objets -->
        <ul>
            <li v-for="(objet, index) in garage" :key="index">
                <!-- Boucle d'un objet en parcourant ses propriété -->
                <p v-for="(voiture, props) in objet" :key="props">{{props}} : {{voiture}}</p>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    data(){
        return{
            tableau: [1,2,3,4,5],
            tableauFruit: ["fraise","pomme","poire"],
            objetVoiture: 
                {
                    marque: "Volkwagen",
                    modele: "Golf 7 R",
                    annee: 2019
                },
            garage: [
                {
                    marque: "Audi",
                    modele: "RS7",
                    annee: 2015
                },
                {
                    marque: "BMW",
                    modele: "M5 Competition",
                    annee: 2019
                }
            ],
            toggleBox: true,
        }
    }
}
</script>
<style>
    .box{
        width: 200px;
        height: 200px;
        border: 1px solid black;
        margin: 0 auto;
    }
    .red{
        background: red;
    }
</style>