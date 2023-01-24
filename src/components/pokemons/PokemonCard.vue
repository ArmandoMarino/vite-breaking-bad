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
    <div class="pokemon-card text-center p-3">
        <img class="img-fluid mb-3" :src="image" :alt="name">
        <p>#{{ number }}</p>
        <p><strong>{{ name }} </strong> </p>
        <p>{{ type }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

.pokemon-card {
    background-color: white;
    border-radius: 50px;

    p {
        font-style: italic;
    }

    img {
        width: 200px;
        height: 200px;
    }
}
</style>