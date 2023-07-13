<script>
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  data() {
    return {
    }
  },
  components:{
    HeaderComponent
  }
}

</script>

<template>

  <header>
   <HeaderComponent></HeaderComponent>
  </header>

  <main>
    <div class="container">

    </div>
  </main>

  <footer>
    
    <section class="footer-links">
      <div class="container"></div>
    </section>

    <section class="footer-info">
      <div class="container"></div>
    </section>

    <section class="footer-socials">
      <div class="container"></div>
    </section>
    
  </footer>

</template>

<style lang="scss" scoped>
@use './assets/scss/main.scss';


main{
  background-color: #1C1C1C;
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
