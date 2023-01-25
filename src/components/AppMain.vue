<script>
import PokemonList from './pokemons/PokemonList.vue';
import DropMenu from './pokemons/DropMenu.vue';
export default {
    name: 'AppMain',
    props: {
        pokemontypes: Array
    },
    components: {
        PokemonList,
        DropMenu
    },
    methods: {
        onSelectedChange(selected) {
            this.$emit('selected-change', selected);
        }
    },
    emits: ['selected-change']
};
</script>


<template>
    <main class="container">
        <drop-menu @selected-change="onSelectedChange" :pokemontypes="pokemontypes"></drop-menu>
        <pokemon-list></pokemon-list>
    </main>
</template>


<style lang="scss">

</style>