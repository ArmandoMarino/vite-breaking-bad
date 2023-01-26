<script>
import axios from 'axios';
import { store } from './data/store';
import AppMain from './components/AppMain.vue';
export default {
  components: {
    AppMain
  },
  data() {
    return {
      pokemontypes: [
        "Ghost",
        "Rock",
        "Electric",
        "Poison",
        "Dark",
        "Fighting",
        "Normal",
        "Dragon",
        "Fire",
        "Fairy",
        "Steel",
        "Ground",
        "Water",
        "Flying",
        "Bug",
        "Ice",
        "Psychic",
        "Grass"
      ],
      store,
      typeFilter: '',
      apiUri: 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
    }
  },
  methods: {
    fetchPokemons(url) {
      store.isLoading = true;
      url += `?eq[type1]=${this.typeFilter}`;
      axios.get(url)
        .then(res => {
          console.log(res);
          store.pokemons = res.data.docs;
        }).catch(error => {
          console.error(error);
          store.pokemons = [];
        }).then(() => {
          store.isLoading = false;
        })
    },
    onSelectedChange(selected) {
      this.typeFilter = selected;
    }
  },
  created() {
    this.fetchPokemons(this.apiUri);
  }
};
</script>

<template>
  <header class="container">
    <img src="./assets/img/pk-logo.png" alt="">
  </header>
  <app-main @selected-change="onSelectedChange" :pokemontypes="pokemontypes"></app-main>
</template>

<style lang="scss">
@use './assets/scss/style.scss';

header {
  display: flex;
  border-radius: 20px;
  justify-content: center;
  min-height: 100px;
  background-color: white;
}
</style>