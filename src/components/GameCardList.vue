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
<div class="container">
    <div class="founds">
        <span>Founds 15 cards</span>
    </div>
    <div class="cards-container">
        <GameCard 
        v-for="card in store.AppList" 
        :key="card.id"
        :cardsData="card"/>
    </div>
</div>
</template>

<style lang="scss" scoped>


.container {
    max-width: 1000px;
    margin-inline: auto;
}
    .cards-container {
        margin-bottom: 2rem;
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
        gap: .5rem;
        padding-bottom: 1rem;
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