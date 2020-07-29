<template>
    <div>
        <h2>Toggle CSS</h2>
        <button v-on:click="toggleColor = !toggleColor">Toggle CSS</button>
        <!-- Style appliquer directment dans un objet (camelCase) -->
        <p :style="{color: 'white', backgroundColor: 'black'}">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eligendi, cum?</p>
        <!-- Appel de la propriétée de style -->
        <p :style="monStyle">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eligendi, cum?</p>
    </div>
</template>
<script>
export default {
    data(){
        return {
            toggleColor: false,
            couleur: "lightblue",
            largeur: 200
        }
    },
    computed: {
        objCSS: function() {
            return {
                red: true,
                box: true
            }
        },
        monStyle: function(){
            return{
                backgroundColor: this.couleur,
                width: this.largeur + "px"
            }
        }
    }
}
</script>
<style>
    .box{
        width: 250px;
        height: 250px;
        border: 1px solid black;
        margin: 0 auto;
    }
    .red{
        background: red;
    }
    .bordure{
        border: 10px solid blue;
    }
</style>