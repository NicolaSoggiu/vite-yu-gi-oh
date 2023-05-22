<script>
    import AppSearch from './components/AppSearch.vue';
    import GameCardList from './components/GameCardList.vue';
    import Results from './components/Results.vue';
    import axios from "axios";
    import { store } from "./store";

export default {
  data() {
    return {
          store,
        }
      },
        components: {
            AppSearch, GameCardList, Results,
  },
  created() {
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0")
      .then((response) => (this.store.CardList = response.data.data));
        }
    }
</script>

<template>
  <body>
    
  <h1>Yu-Gi-Ho Api</h1>

  <main>
    <AppSearch/>
    <GameCardList/>
    <Results/>
  </main>
</body>
</template>

<style lang="scss">
@use "./assets/styles/general.scss";

  h1 {
    width: 100%;
    padding: 1rem;
    background-color: white;
  }
</style>
