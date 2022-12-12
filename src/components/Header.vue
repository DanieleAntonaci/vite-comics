<script >
export default {
  name: 'Header',
  data() {
    return {
      informationNavBar: [
        {
          name: 'CHARACTERS',
          activeElement: false
        },
      ]
    }
  }
}
</script>

<template>
  <header>
    <img src="/img/dc-logo.png" alt="Logo DC">
    <nav>
      <ul>
        <li>
          <a href="#">Caracter</a>
        </li>
        <li>
          <a href="#">Caracter</a>
        </li>
        <li>
          <a href="#">Caracter</a>
        </li>
        <li>
          <a href="#">Caracter</a>
        </li>
        <li>
          <a href="#">Caracter</a>
        </li>
        <li>
          <a href="#">Caracter</a>
        </li>
        <li>
          <a href="#">Caracter</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
header {
  @include center();

  ul {
    display: flex;

    & li {
      padding: 0 10px;

    }
  }
}
</style>
