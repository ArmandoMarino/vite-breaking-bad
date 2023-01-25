<script>
export default {
    name: 'DropMenu',
    props: {
        pokemontypes: Array
    },
    data() {
        return {
            term: ''
        }

    }
}
</script>

<template>
    <div class="dropdown">
        <label for="pokemons">Choose type:</label>
        <select name="pokemons" id="pokemons">
            <option v-for="pokemontype in pokemontypes" :value="pokemontype">{{ pokemontype }}</option>
        </select>
    </div>
</template>

<style>

</style>