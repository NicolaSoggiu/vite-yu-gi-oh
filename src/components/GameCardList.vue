<script>
    import GameCard from './GameCard.vue'
    import { store } from "../store"
    
    export default {
        data() {
            return {
                store,
            }
        },
        components: {
            GameCard,  
        }
    }
</script>

<template>
    <div class="cards-container">
        <GameCard 
        v-for="card in store.CardList" 
        :key="card.id"
        class="card"
        :cardsData="card"/>
    </div>
</template>

<style lang="scss" scoped>

</style>