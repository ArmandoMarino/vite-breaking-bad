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
      store
    }
  },
  methods: {
    fetchPokemons(url) {
      axios.get(url)
        .then(res => {
          console.log(res);
          store.pokemons = res.data.docs;
        })
    }
  },
  created() {
    this.fetchPokemons(store.apiUri);
  }
};

</script>

<template>
  <header class="container">
    <img src="./assets/img/pk-logo.png" alt="">
  </header>
  <app-main></app-main>
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