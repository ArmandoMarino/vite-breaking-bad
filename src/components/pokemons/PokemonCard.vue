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
    <div class="col pokemon-card text-center">
        <div class=" interior-card p-3">
            <img class="img-fluid mb-3" :src="image" :alt="name">
            <p>#{{ number }}</p>
            <p><strong>{{ name }} </strong> </p>
            <p>{{ type }}</p>
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

.pokemon-card {

    .interior-card {
        background-color: white;

        p {
            font-style: italic;
        }

        img {
            width: 200px;
            height: 200px;
        }
    }
}
</style>