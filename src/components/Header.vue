<script >
export default {
  name: 'Header',
  data() {
    return {

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
  display: flex;
  justify-content: space-between;

  ul {
    display: flex;

    & li {
      padding: 0 10px;

    }
  }
}
</style>
