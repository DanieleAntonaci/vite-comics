<script>

export default {
    props: {
        thumb: String,
        title: String
    },
}
</script>

<template>

            <!-- card -->
            <div class="card">
                <img :src="thumb" :alt="title">
                
                <a href="#">{{ title }}</a>
            </div>
            
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;


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
</style>