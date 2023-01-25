<script>
export default {
    name: 'DropMenu',
    data() {
        return {
            value: '',
            selected: 'Ghost'
        }
    },
    props: {
        pokemontypes: Array
    },
    emits: ['value-change']
}
</script>

<template>
    <div class="dropdown">
        <label for="pokemons">Choose type:</label>
        <select v-model="selected" name="pokemons" id="pokemons">
            <option v-for="pokemontype in pokemontypes" :value="pokemontype" @click="$emit('value-change', value)">
                {{ pokemontype }}</option>
        </select>
    </div>
</template>

<style>

</style>