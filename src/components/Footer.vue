<script>
import Merchandise from './Merchandise.vue'

export default {
    components: {
        Merchandise
    },
    data() {
        return {

            footerElement: [

                {
                    title: 'DC COMICS',
                    listLink: [
                        {
                            text: 'Characters',
                            url: '#'
                        },
                        {
                            text: 'Comics',
                            url: '#'
                        },
                        {
                            text: 'Movies',
                            url: '#'
                        },
                        {
                            text: 'TV',
                            url: '#'
                        },
                        {
                            text: 'Games',
                            url: '#'
                        },
                        {
                            text: 'Videos',
                            url: '#'
                        },
                        {
                            text: 'News',
                            url: '#'
                        },
                    ]
                }, {
                    title: 'SHOP',
                    listLink: [
                        {
                            text: 'Shop DC',
                            url: '#'
                        },
                        {
                            text: 'Shop DC Collectivles',
                            url: '#'
                        },
                    ]
                }, {
                    title: 'DC',
                    listLink: [
                        {
                            text: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            text: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            text: 'Ad Choises',
                            url: '#'
                        },
                        {
                            text: 'Adverting',
                            url: '#'
                        },
                        {
                            text: 'Jobs',
                            url: '#'
                        },
                        {
                            text: 'Subscription',
                            url: '#'
                        },
                        {
                            text: 'Talent Workshps',
                            url: '#'
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            text: 'Ratings',
                            url: '#'
                        },
                        {
                            text: 'Shop Help',
                            url: '#'
                        },
                        {
                            text: 'Contact Us',
                            url: '#'
                        },
                    ]
                }, {
                    title: 'SITES',
                    listLink: [
                        {
                            text: 'DC',
                            url: '#'
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            text: 'DC Kids',
                            url: '#'
                        },
                        {
                            text: 'DC Universe',
                            url: '#'
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#'
                        }
                    ]
                }
            ],
            imgSocial: [
                {
                    img: 'img/footer-facebook.png',
                    link: '#'
                }, {
                    img: 'img/footer-twitter.png',
                    link: '#'
                }, {
                    img: "img/footer-youtube.png",
                    link: '#'
                }, {
                    img: "img/footer-pinterest.png",
                    link: '#'
                }, {
                    img: "img/footer-periscope.png",
                    link: '#'
                },
            ]
        }
    }
}
</script>

<template>
    <!-- modulo linea blu/ merchandise -->
    <Merchandise/>


    <section id="navSection">
        <div class="container">
            <div class="linkFooter">

                <div v-for="element in footerElement">

                    <h3>{{ element.title }}</h3>

                    <ul>

                        <li v-for="link in element.listLink">
                            <a :href="link.url">
                                {{ link.text }}
                            </a>
                        </li>

                    </ul>

                </div>

            </div>

            <div class="img-footer">

                <img src="/img/dc-logo-bg.png" alt="">

            </div>

        </div>

    </section>

    <section id="footerSocial">

        <div class="container">

            <button>
                SIGN-UP NOW!
            </button>

            <div>

                <h3>FOLLOW US</h3>
                
                <a  v-for="img in imgSocial"  :href="img.link">
                    <img :src="img.img" alt="Social icon">
                </a>
            
            </div>

        </div>

    </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

#navSection {
    background-image: url('/img/footer-bg.jpg');
    padding: 0;
    height: 400px;


    & .linkFooter {
        @include center('onlyFlex');
        height: 400px;
        flex-direction: column;
        flex-wrap: wrap;
        padding: 30px 0;

        & h3 {
            color: $secondaryColor;
            padding: 15px 0;
        }

        & ul li a {
            color: rgb(150, 150, 150);
            font-size: 15px;
            text-decoration: none;
            line-height: 25px;
            padding-right: 30px;
        }
    }

    .img-footer {
        height: 400px;
        overflow: hidden;

        & img {
            object-position: 0 -100px;

        }
    }

}

#footerSocial {
    background-color: #303030;
    height: 100px;
    padding: 20px;
    z-index: 20;

    button {
        color: $secondaryColor;
        background-color: #303030;
        box-shadow: none;
        border: $primaryColor 2px solid;
        padding: 15px 20px;
        font-size: 16px;
    }

    div {
        @include center('horizontal');

        h3 {
            color: $primaryColor;
        }

        a {
            padding-left: 15px;
        }
    }
}
</style>