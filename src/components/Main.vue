<script>
import CurrentSeries from './CurrentSeries.vue';
export default {
    components: {
        CurrentSeries
    }

}
</script>

<template>
    <main>
        <section id="jubmbotron">
            
        </section>
        <CurrentSeries/>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

main {
    background-color: #1c1c1c;
    color: $secondaryColor;

    #jubmbotron {
        background-image: url('/img/jumbotron.jpg');
        background-size: cover;
        height: 300px;
        width: 100%;
        color: $secondaryColor;
    }



}
</style>