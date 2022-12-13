<script >
export default {
  name: 'Header',
  data() {
    return {
      informationNavBar: [
        {
          text: 'CHARACTERS',
          url: '#',
          activeElement: true
        },
        {
          text: 'COMICS',
          url: '#',
          activeElement: false
        },
        {
          text: 'MOVIES',
          url: '#',
          activeElement: false
        },
        {
          text: 'TV',
          url: '#',
          activeElement: false
        },
        {
          text: 'GAMES',
          url: '#',
          activeElement: false
        },
        {
          text: 'COLLECTIBLES',
          url: '#',
          activeElement: false
        },
        {
          text: 'VIDEOS',
          url: '#',
          activeElement: false
        },
        {
          text: 'FANS',
          url: '#',
          activeElement: false
        },
        {
          text: 'NEWS',
          url: '#',
          activeElement: false
        },
        {
          text: 'SHOP',
          url: '#',
          activeElement: false
        },
      ]
    }
  }
}
</script>

<template>
  <header>
    <div class="container">

      <img src="/img/dc-logo.png" alt="Logo DC">


      <nav>
        <ul>

          <li  v-for="(element, index) in informationNavBar" :key="index">
            <a :class="{ active: element.activeElement }" :href="element.link">
              {{ element.text }}
            </a>
          </li>
          
        </ul>
      </nav>

    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

header {
  padding: 10px 0;
  background-color: $secondaryColor;
  position: sticky;
  top: 0;


  .container {
    img {
      height: 80px;
    }

    ul {
      @include center('onlyFlex');

      li {
        padding: 0 10px;

        a {
          color: black;
          text-decoration: none;
          font-weight: 600;
          font-size: 14px;
          padding-bottom: 37px;
        }

        & :hover,
        & .active {
          color: $primaryColor;
          border-bottom: 5px solid $primaryColor;
        }
      }
    }
  }
}
</style>
