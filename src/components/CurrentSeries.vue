<script>

export default {
    data() {
        return {

        }
    },
}
</script>

<template>
    <main>
        <div class="container">
            <h2>
            CURRENT SERIES
            </h2>

            <!-- card -->
            <div class="card">
                <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX" alt="">
                
                <a href="#">ACTION COMICS</a>
            </div>
            
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

main {
    min-height: 600px;
    background-color: #1c1c1c;
    color: $secondaryColor;

    .container {
        position: relative;
        width: 100%;
        @include center('onlyFlex');
        justify-content: flex-start;
        flex-wrap: wrap;

        h2 {
            background-color: $primaryColor;
            padding: 10px 20px;
            position: absolute;
            top: -30px;
        }

        .card {
            width: calc((100% / 6) - 20px);
            margin: 0 10px;

            img {
                width: 100%;
                height: 14vw;
                max-height: 180px;
                overflow: hidden;
                object-fit: cover;
                margin-top: 40px;
            }

            a {
                color: $secondaryColor;
                display: block;
                padding-top: 10px;
                font-size: 14px;
            }
        }


    }
}
</style>