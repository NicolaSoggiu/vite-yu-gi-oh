<script>
export default {
    props: {
        cardsData: Object,
    }
}
</script>

<template>
    <img :src="cardsData.card_images.image_url" :alt="cardsData.name">
    <h2> {{ cardsData.name }} </h2>
</template>

<style lang="scss" scoped>

</style>