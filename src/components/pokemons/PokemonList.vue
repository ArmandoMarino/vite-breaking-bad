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
    <section id="pokemons container">
        <div class="row m-3 row-cols-2 row-cols-lg-5 g-2 g-lg-3">
            <pokemon-card v-for="pokemon in store.pokemons" :key="pokemon.id" :number="pokemon.number"
                :name="pokemon.name" :image="pokemon.imageUrl" :type="pokemon.type1"></pokemon-card>
        </div>
    </section>
</template>

<style lang="scss" scoped>
#pokemons {
    height: 100vh;
    overflow-y: auto;
}
</style>