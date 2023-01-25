<script>
export default {
    name: 'DropMenu',
    props: {
        pokemontypes: Array
    }
}
</script>

<template>
    <div class="dropdown">
        <label for="cars">Choose type:</label>

        <select name="cars" id="cars">
            <option v-for="pokemontype in pokemontypes" value="volvo">{{ pokemontype }}</option>
        </select>
    </div>
</template>

<style>

</style>