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
        <div class="content-footer">
            <div class="container">
                <div class="footer-links">
                    <div class="links">
                        <h3>DC COMICS</h3>
                        <nav>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                        </nav>
                        <h3>SHOP</h3>
                        <nav>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </nav>
                    </div>
                    <div class="links">
                        <h3>DC</h3>
                        <nav>
                            <ul>
                                <li><a href="#">Terms Of Use</a></li>
                                <li><a href="#">Privacy policy (New)</a></li>
                                <li><a href="#">Ad Chois</a></li>
                                <li><a href="#">Advertising</a></li>
                                <li><a href="#">Jobs</a></li>
                                <li><a href="#">Subscriptions</a></li>
                                <li><a href="#">Talent Workshop</a></li>
                                <li><a href="#">CPSC Cerification</a></li>
                                <li><a href="#">Ratings</a></li>
                                <li><a href="#">Shop Help</a></li>
                                <li><a href="#">Contacts Us</a></li>

                            </ul>
                        </nav>
                    </div>
                    <div class="links">
                        <h3>SITES</h3>
                        <nav>
                            <ul>
                                <li><a href="#">DC</a></li>
                                <li><a href="#">Mad Magazine</a></li>
                                <li><a href="#">DC Kids</a></li>
                                <li><a href="#">DC Universe</a></li>
                                <li><a href="#">DC Power Visa</a></li>
                            </ul>
                        </nav>
                    </div>
                </div>
                <div class="footer-image">
                    <img src="/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
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
            padding: 30px 10px;
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

    .content-footer {
        background-image: url('./img/footer-bg.jpg');
        background-size: cover;

        .container {
            position: relative;
            padding: 30px 0;
            @include space-between;

            .footer-links {
                display: flex;

                .links {
                    margin-right: 30px;

                    ul {
                        list-style-type: none;

                        li a {
                            text-decoration: none;
                            color: $grey;

                            &:hover,
                            &:active {
                                color: $white;
                            }
                        }
                    }

                    h3 {
                        color: $white;
                        padding: 15px 0;
                    }
                }
            }

            .footer-image {
                img {
                    position: absolute;
                    top: 0;
                    right: 0;
                    transform: translateY(-20%);
                }
            }
        }
    }
}</style>