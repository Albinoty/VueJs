<template>
    <div>
        <h2>Toggle CSS</h2>
        <button v-on:click="toggleColor = !toggleColor">Toggle CSS</button>
        <!-- on attribue la class à appliquer -->
        <!-- Ici on indique une objet qui applique la class red si toggleColor est true -->
        <div class="box"
        v-bind:class="{ red : toggleColor }"
        ></div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            // on declare une propriété qui sera en false
            toggleColor: false
        }
    },
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
</style>