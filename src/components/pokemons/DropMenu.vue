<script>
export default {
    name: 'DropMenu',
    data() {
        return {
            selected: ''
        }
    },
    props: {
        pokemontypes: Array
    },
    emits: ['selected-change']
}
</script>

<template>
    <div class="dropdown">
        <label for="pokemons">Choose type:</label>
        <select v-model="selected" name="pokemons" id="pokemons" @click="$emit('selected-change', selected)">
            <option value="">---</option>
            <option v-for="pokemontype in pokemontypes" :value="pokemontype">{{ pokemontype }}</option>
        </select>
    </div>
</template>

<style>

</style>