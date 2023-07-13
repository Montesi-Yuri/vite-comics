<script>
import Component1 from './components/Component1.vue'

export default {
  data() {
    return {
    }
  },
  components:{
    Component1
  }
}

</script>

<template>

  <header>
    <nav>

      <div>
        <img src="" alt="">
      </div>

      <ul>

        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>

      </ul>
    </nav>
  </header>

  <main>
  </main>

  <footer>

    <section class="footer-links"></section>

    <section class="footer-info"></section>

    <section class="footer-socials"></section>

  </footer>

</template>

<style lang="scss" scoped>
@use './assets/scss/main.scss';

header{
  background-color: bisque;
  width: 100%;
  height: 100px;
  border: 1px solid black;
    nav{
      display: flex;
    }
}

main{
  background-color: lightblue;
  width: 100%;
  height: 100px;
  border: 1px solid black;
}

footer{
  width: 100%;
  border: 1px solid black;
  
  section{
    height: 100px;

    &.footer-links{
      background-color: lightgreen;
    }
    &.footer-info{
      background-color: orange;
    }
    &.footer-socials{
      background-color: grey;
    }
  }
}

</style>
