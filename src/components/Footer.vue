<script>
export default {
    data() {
        return {
            merchandiseElements: [
                {
                    text: "DICITAL COMICS",
                    img: '/img/buy-comics-digital-comics.png',
                    link: '#'
                },
                {
                    text: "DC MERCHANDISE",
                    img: '/img/buy-comics-merchandise.png',
                    link: '#'
                },
                {
                    text: "SUBSCRIPTON",
                    img: '/img/buy-comics-shop-locator.png',
                    link: '#'
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    img: '/img/buy-comics-subscriptions.png',
                    link: '#'
                },
                {
                    text: "DC POWER VISA",
                    img: '/img/buy-dc-power-visa.svg',
                    link: '#'
                },
            ],
            footerElement: [

                {
                    title: 'DC COMICS',
                    listLink: [
                        {
                            text: 'Characters',
                            url: '#',
                            activeElement: true
                        },
                        {
                            text: 'Comics',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'Movies',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'TV',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'Games',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'Videos',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'News',
                            url: '#',
                            activeElement: false
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
    <section id="merchandise">
            <ul class="container">
                <li v-for="(element, index) in merchandiseElements" :key="index">
                    <img :src="element.img" alt="">
                    <a :href="element.link">{{ element.text }}</a>
                </li>
            </ul>
    </section>

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
#merchandise {
    background-color: #0282f9;


    & ul {
        display: flex;
        align-items: center;
        padding: 40px 0;



        & li {
            display: flex;
            align-items: center;
            justify-content: space-between;


            & img {
                height: 50px;
            }

            & a {
                color: white;
                text-decoration: none;
                padding: 0 10px;
                font-size: 13px;
            }
        }
    }
}

#navSection {
    background-image: url('/img/footer-bg.jpg');
    padding: 0;
    height: 400px;


    & .linkFooter {
        height: 400px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        padding: 30px 0;

        & h3 {
            color: white;
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

    & button {
        color: white;
        background-color: #303030;
        box-shadow: none;
        border: #0282f9 2px solid;
        padding: 15px 20px;
        font-size: 16px;
    }

    & div {
        display: flex;
        align-items: center;

        & h3 {
            color: #0282f9;
        }

        & a {
            padding-left: 15px;
        }
    }
}
</style>