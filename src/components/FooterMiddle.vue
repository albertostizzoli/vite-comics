<template>
    <div class="content-footer">
        <div class="container">
            <div class="footer-links">
                <div class="links">
                    <h3>DC COMICS</h3>
                    <nav>
                        <ul>
                            <li v-for="index in dcComics" :key="index">
                            {{ index.text }}
                        </li>
                        </ul>
                    </nav>
                    <h3>SHOP</h3>
                    <nav>
                        <ul>
                            <li v-for="index in Shop" :key="index">
                            {{ index.text }}
                        </li>
                        </ul>
                    </nav>
                </div>
                <div class="links">
                    <h3>DC</h3>
                    <nav>
                        <ul>
                            <li v-for="index in DC" :key="index">
                            {{ index.text }}
                        </li>
                        </ul>
                    </nav>
                </div>
                <div class="links">
                    <h3>SITES</h3>
                    <nav>
                        <ul>
                            <li v-for="index in Sites" :key="index">
                            {{ index.text }}
                        </li>
                        </ul>
                    </nav>
                </div>
            </div>
            <div class="footer-image">
                <img src="/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'FooterMiddle',
    data(){
        return {
            dcComics: [
                {
                    text: 'Characters'
                },
                {
                    text: 'Comics'
                },
                {
                    text: 'Movies'
                },
                {
                    text: 'TV'
                },
                {
                    text: 'Games'
                },
                {
                    text: 'Videos'
                },
                {
                    text: 'News'
                },
               ],
               Shop:[
                {
                    text: 'Shop DC'
                },
                {
                    text: 'Shop DC Collectibles'
                }
               ],
               DC:[
                {
                    text: 'Terms Of Use',
                },
                {
                    text: 'Privacy policy (New)',
                },
                {
                    text: 'Ad Choices',
                },
                {
                    text: 'Advertising',
                },
                {
                    text: 'Jobs',
                },
                {
                    text: 'Subscriptions',
                },
                {
                    text: 'Talent Workshops',
                },
                {
                    text: 'CPSC Certificates',
                },
                {
                    text: 'Ratings',
                },
                {
                    text: 'Shop Help',
                },
                {
                    text: 'Contact Us',
                },
               ],
               Sites: [
                {
                    text: 'DC',
                },
                {
                    text: 'MAD Magazine',
                },
                {
                    text: 'DC Kids',
                },
                {
                    text: 'DC Universe',
                },
                {
                    text: 'DC Power Visa',
                },
               ]
        }
    }

}
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

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

                    li{
                        color: $grey;

                        &:hover,
                        &:active {
                            color: $white;
                            cursor: pointer;
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
                transform: translateY(-25%);
            }
        }
    }
}
</style>