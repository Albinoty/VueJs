<template>
    <div>
        <h2>Toggle CSS</h2>
        <button v-on:click="toggleColor = !toggleColor">Toggle CSS</button>
        <!-- A la place d'écrire l'objet en question, on peut le faire appel direcrement -->
        <div class="box" v-bind:class="objCSS"></div>
        <!-- il est possible d'ajouter un tableau et de faire varier les class css -->
        <div class="box" v-bind:class="[objCSS, 'bordure']"></div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            toggleColor: false,
        }
    },
    computed: {
        objCSS: function() {
            return {
                red: true,
                box: true
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