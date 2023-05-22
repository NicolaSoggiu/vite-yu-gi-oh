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
    <div class="founds">
        <span>Founds 15 cards</span>
    </div>
    <div class="cards-container">
        <GameCard 
        v-for="card in store.CardList" 
        :key="card.id"
        :cardsData="card"/>
    </div>
</template>

<style lang="scss" scoped>

    .cards-container {
        max-width: 1000px;
        margin-inline: auto;
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
        gap: .5rem;
        padding: 1rem;
        background-color: white;
    }

    .founds {
        max-width: 1000px;
        margin-inline: auto;
        padding: 1rem;
        color: white;
        background-color: #212529;
    }
</style>