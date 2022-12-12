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
                            text: 'Shop DC',
                            url: '#'
                        },
                        {
                            text: 'Shop DC Collectivles',
                            url: '#'
                        },
                    ]
                }, {
                    title: 'SITES',
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
                }
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
    padding: 40px 0;

    & h3 {
        color: white;

    }

    & .linkFooter {}

    & ul li a {
        color: rgb(150, 150, 150);
        font-size: 15px;
        text-decoration: none;
        line-height: 23px;
    }

}
</style>