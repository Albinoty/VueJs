<template>
    <div>
        <button v-on:click="toggleBox = !toggleBox">ToggleBox</button>
        <!-- if, else -->
        <div v-if="toggleBox" class="box red"></div>
        <p v-else>Sinon</p>
        <!-- if, else-if, else -->
        <button @click="num--">-1</button>
        <button @click="num++">-1</button>
        <p v-if="num === 1">Le numéro est 1</p>
        <p v-else-if="num === 2">Le numéro est 2</p>
        <p v-else-if="num === 3">Le numéro est 3</p>
        <p v-else>Le numéro n'est ni 1, ni 2, ni 3</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            toggleBox: true,
            num: 1
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