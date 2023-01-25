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
        <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            Pokemon Types
        </button>
        <ul class="dropdown-menu">
            <li v-for="pokemontype in pokemontypes"><a class="dropdown-item" href="#"></a></li>
        </ul>
    </div>
</template>

<style>

</style>