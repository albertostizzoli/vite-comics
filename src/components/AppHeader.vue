<template>
    <header class="container">
        <a href="#">
            <img src="/img/dc-logo.png" alt="">
        </a>
        <nav>
            <ul>
                <li v-for="(item, index) in list" :key="index">
                    <a :href="item.url">{{ item.label }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            list: [
                {
                    label: 'characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'tv',
                    url: '#',
                    active: false
                },
                {
                    label: 'games',
                    url: '#',
                    active: false
                },
                {
                    label: 'collectibles',
                    url: '#',
                    active: false
                },
                {
                    label: 'videos',
                    url: '#',
                    active: false
                },
                {
                    label: 'fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'news',
                    url: '#',
                    active: false
                },
                {
                    label: 'shop',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

header {
    padding: 1rem;
    @include space-between;

    img {
        width: 80px;
    }

    ul {
        list-style-type: none;
        text-transform: uppercase;
        margin-left: 30px;

        li {
            display: inline-block;
            font-size: 15px;
            padding: 10px;

            a {
                color: $black;
                text-decoration: none;

                &:hover,
                &:active {
                    color: $light-blue;
                    border-bottom: 5px solid $light-blue;
                }
            }
        }
    }
}
</style>