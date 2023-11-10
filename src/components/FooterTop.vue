<template>
    <footer>
        <div class="top-footer container">
            <ul>
                <li v-for="(item, index) in list" :key="index">
                    <img :src="`/img/${item.image}`" alt="logos">
                    <a :href="item.url">{{ item.label }}</a>
                </li>
            </ul>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterTop',
    data() {
        return {
            list: [
                {
                    image: 'buy-comics-digital-comics.png',
                    label: 'digital comics',
                    url: '#'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    label: 'dc merchandise',
                    url: '#'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    label: 'subscription',
                    url: '#'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    label: 'comic shop locator',
                    url: '#'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    label: 'dc power visa',
                    url: '#'
                },
            ]
        }
    }

}
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

footer {
    background-color: $light-blue;

    .top-footer {
        position: relative;
        z-index: 1000;

        img {
            width: 40px;
        }

        ul {
            list-style-type: none;
            padding: 40px 10px;
            @include space-between;

            li {
                display: flex;
                align-items: center;

                a {
                    text-transform: uppercase;
                    color: $white;
                    text-decoration: none;
                    padding: 3px 3px;
                }
            }
        }
    }

}
</style>