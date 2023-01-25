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
}
</script>


<template>
    <main class="container">
        <drop-menu></drop-menu>
        <pokemon-list></pokemon-list>
    </main>
</template>


<style lang="scss">

</style>