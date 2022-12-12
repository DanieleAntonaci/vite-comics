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
header {
  margin: 20px 0;
  position: sticky;


  & .container {


    ul {
      display: flex;

      & li {
        padding: 0 10px;

        & a {
          color: black;
          text-decoration: none;
          font-weight: 600;
          font-size: 14px;

        }

        & :hover,
        &.active {
          color: blue;
          margin-bottom: 2px solid blue;
        }
      }
    }
  }
}
</style>
