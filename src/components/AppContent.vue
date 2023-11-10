<template>
    <main>
        <div class="jumbotron">
            <img src="/img/jumbotron.jpg" alt="Dc Characters">
        </div>
        <div class="container">
            <span class="label">Current series</span>
            <div class="row">
                <CardSeries v-for="(item, index) in array_series" :key="index" :series_card="item" />
            </div>
            <div class="bottom-btn">
                <button class="btn-light-blue">Load more</button>
            </div>
        </div>
    </main>
</template>

<script>
import list_series from './data/listSeries.js';
import CardSeries from './cards/CardSeries.vue';
export default {
    name: 'AppContent',
    components: {
        CardSeries,
    },
    data() {
        return {
            array_series: list_series
        }
    },
}
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

main {
    background-color: $black;

    .jumbotron {
        img {
            width: 100%;
            height: 350px;
            object-fit: cover;
            object-position: top;
        }
    }

    .container {
        position: relative;

        .label {
            @include bg-light-blue;
            font-size: 25px;
            font-weight: bold;
            padding: 10px;
            position: absolute;
            top: 0;
            left: 0;
            transform: translateY(-50%);
        }

        .row {
            padding: 30px 15px;
            display: flex;
            flex-wrap: wrap;
        }
    }

    .bottom-btn {
        text-align: center;

        .btn-light-blue {
            @include bg-light-blue;
            padding: 10px 40px;
            font-weight: bold;
            border: none;
            margin-bottom: 20px;
            cursor: pointer;
        }
    }
}
</style>