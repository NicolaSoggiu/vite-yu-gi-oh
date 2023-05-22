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
  <h1>Yu-Gi-Ho!</h1>

  <main>
    <AppSearch/>
    <GameCardList/>
    <Results/>
  </main>
</template>

<style lang="scss">

</style>
