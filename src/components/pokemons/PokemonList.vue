<script>
import { store } from '../../data/store';
import PokemonCard from './PokemonCard.vue';
export default {
    name: 'PokemonList',
    components: {
        PokemonCard
    },
    data() {
        return { store }
    }
};
</script>

<template>
    <section id="pokemons">
        <div v-if="store.isLoading" class="text-center">Loading...</div>
        <div v-else class="row m-3 row-cols-2 row-cols-lg-5 g-2 g-lg-3">
            <pokemon-card v-for="pokemon in store.pokemons" :key="pokemon.id" :number="pokemon.number"
                :name="pokemon.name" :image="pokemon.imageUrl" :type="pokemon.type1"></pokemon-card>
        </div>
    </section>


</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

#pokemons {
    height: 70vh;
    border-radius: 20px;
    overflow-y: auto;
    background-color: $secondary-bg;
}
</style>