<script>
export default {
    name: 'PokemonCard',
    props: {
        number: String,
        name: String,
        image: String,
        type: String,
    }
};
</script>

<template>
    <div class="pokemon-card text-center p-2">
        <img class="img-fluid mb-3" :src="image" :alt="name">
        <p>#{{ number }}</p>
        <p>{{ name }}</p>
        <p>{{ type }}</p>
    </div>
</template>

<style>

</style>