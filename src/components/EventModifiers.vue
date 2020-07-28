<template>
    <div>
        <!-- Le Once va permettre de faire une seul fois l'event  -->
        <button v-on:click.once="foo">Click me</button>
        <!-- le stop permet d'éviter que l'enfant utilise l'event du parent, c'est à dire qui propagation. Du coup, ils sont indépendants. -->
        <p v-on:click="foo">
            Lorem, ipsum.
            <button v-on:click.stop="foo">Click me</button>
        </p>
        <!-- Previens le comportement par défaut -->
        <form v-on:submit.prevent="onSubmit">
            <button>Valider</button>
        </form>
    </div>
</template>

<script>
export default {
    methods: {
        foo: function(){
            console.log("Click")
        }
    }
}
</script>