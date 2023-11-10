<template>
    <div class="card">
        <div>
            <img :src="series_card.thumb" alt="Card">
        </div>
        <div class="card-title">
            <span>{{ series_card.series }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardSeries',
    props:{
        series_card: Object
    }
}
</script>

<style lang="scss">

.card {
    width: calc(100% / 6);
    padding: 15px;
    display: flex;
    flex-direction: column;

    img {
        object-position: left top;
        object-fit: cover;
        width: 100%;
        height: 150px;
    }

    .card-title {
        color: white;
        text-transform: uppercase;
    }
}
</style>