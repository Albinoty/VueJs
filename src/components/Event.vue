<template>
  <div>
    <h2>v-on</h2>
    <!-- le {{}} appele une donnée en question -->
    <p>Mon compteur:{{compteur}}</p>
    <div>
        <!-- v-on permet d'utiliser un événement -->
        <!-- :click est de type click -->
        <button v-on:click="augmente">+1</button>
        <button v-on:click="diminue">-1</button>
    </div>
    <canvas v-on:mousemove="coords"></canvas>
    <p>Coords: {{ x }} / {{ y }}</p>
  </div>
</template>

<script>
export default {
    name: "Event",
    data() {
        return {
            compteur: 0,
            x: 0,
            y: 0
        }
    },
    components: {

    },
    methods: {
        augmente: function() {
            this.compteur++;
        },
        diminue: function() {
            this.compteur--;
        },
        coords: function(e){
            // console.log(e)
            this.x = e.offsetX;
            this.y = e.offsetY;
        }
    }
}
</script>

<style>
    canvas{
        width: 300px;
        height: 200px;
        border: 1px solid black;
    }
</style>