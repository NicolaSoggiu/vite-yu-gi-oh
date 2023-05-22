<script>
    import AppSearch from './components/AppSearch.vue';
    import GameCardList from './components/GameCardList.vue';
    import Results from './components/Results.vue';

    export default {
        components: {
            AppSearch, GameCardList, Results,
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
