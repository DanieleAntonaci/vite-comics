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
  <main>

  </main>
</template>

<style lang="scss">
@use './style/general.scss' as *;
@use './style/partials/variables' as *;
@use './style/partials/mixin' as *;

main {
  background-color: black;
  height: 100px;
  width: 100%;
}
</style>
 