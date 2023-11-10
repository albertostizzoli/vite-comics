<template>
    <div class="bottom-footer">
        <div class="container">
            <a href="#" class="login">SIGN UP NOW!</a>
            <nav>
                <h2>FOLLOW US</h2>
                <ul>
                    <li v-for="(item, index) in socials" :key="index">
                        <a href="/">
                            <img :src="`/${item}`" alt="Socials">
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterBottom',
    data() {
        return {
            socials: [
                'img/footer-facebook.png',
                'img/footer-periscope.png',
                'img/footer-pinterest.png',
                'img/footer-twitter.png',
                'img/footer-youtube.png'
            ]
        }
    }
}
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

.bottom-footer {
    background-color: #303030;
    position: relative;
    z-index: 1000;

    .container {
        height: 100px;
        @include space-between;

        .login {
            text-decoration: none;
            font-size: 20px;
            padding: 15px;
            color: $white;
            border: 2px solid $light-blue;
        }

        nav {
            display: flex;

            h2 {
                color: $light-blue;
                padding: 8px;
            }

            ul {
                list-style-type: none;

                li {
                    display: inline-block;
                    padding: 6px;
                }
            }
        }
    }
}
</style>