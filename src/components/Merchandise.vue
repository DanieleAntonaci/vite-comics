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

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

#merchandise {
    background-color: $primaryColor;


    & ul {
        @include center('horizontal');
        padding: 40px 0;



        & li {
            @include center('horizontal');
            justify-content: space-between;


            & img {
                height: 50px;
            }

            & a {
                color: $secondaryColor;
                text-decoration: none;
                padding: 0 10px;
                font-size: 13px;
            }
        }
    }
}
</style>