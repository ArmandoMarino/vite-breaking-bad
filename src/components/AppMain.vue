<script>
import PokemonList from './pokemons/PokemonList.vue';
export default {
    name: 'AppMain',
    components: {
        PokemonList
    },
}
</script>


<template>
    <main class="container">
        <pokemon-list></pokemon-list>
    </main>
</template>


<style lang="scss">

</style>