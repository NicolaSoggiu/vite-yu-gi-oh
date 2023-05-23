<script>
export default {
    props: {
        cardsData: Object,
    }
}
</script>

<template>
    <div class="card">
        <img :src="cardsData.card_images[0].image_url" :alt="cardsData.name">
        <div class="description">
            <h2> {{ cardsData.name }} </h2>
            <span>{{ cardsData.archetype ? cardsData.archetype : "Undefined" }}</span>
        </div>
        
    </div>
</template>

<style lang="scss" scoped>

    .card {   
        width: calc((100% - 12rem) / 5);
        background-color: #D48F38;
        img {
            width: 100%;
        }
        h2 {
            color: white;
            text-align: center;
            font-size: .8rem;
        }
        .description {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 1rem;
            text-align: center;
            gap: 1rem;
        }
    }
</style>