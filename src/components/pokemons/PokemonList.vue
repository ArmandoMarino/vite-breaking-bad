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
        <div class="row mt-2 g-4 row-cols-2 row-cols-md-3 row-cols-lg-4">
            <pokemon-card v-for="pokemon in store.pokemons" :key="pokemon.id" :number="pokemon.number"
                :name="pokemon.name" :image="pokemon.imageUrl" :type="pokemon.type1"></pokemon-card>
        </div>
    </section>
</template>

<style lang="scss" scoped>
#pokemons {
    height: 0vh;
    overflow-y: auto;
}
</style>