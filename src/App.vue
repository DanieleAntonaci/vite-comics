<script >
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,

  }
}
</script>

<template>
  <Header/>

</template>

<style lang="scss">
@use './style/general.scss' as *;
@use './style/partials/variables' as *;
</style>
