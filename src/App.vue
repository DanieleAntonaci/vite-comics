<script >
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<template>
  <Header/>
  <main>
   <div class="container">
    <h2>
    -->Content goes here 

    </h2>
   </div>
  </main>
  <Footer />
</template>

<style lang="scss">
@use './style/general.scss' as *;
@use './style/partials/variables' as *;
@use './style/partials/mixin' as *;

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

main {
  background-color: black;
  height: 100px;
  width: 100%;
  color: white;
}
</style>
 