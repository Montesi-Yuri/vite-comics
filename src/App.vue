<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue'

export default {
  data() {
    return {
    }
  },
  components:{
    HeaderComponent,
    FooterComponent,

  }
}

</script>

<template>

  <header>
   <HeaderComponent></HeaderComponent>
   
  </header>

  <main>
    <div class="container">
      <h3>Missing main content</h3>
    </div>
  </main>

  <footer>
    
    <FooterComponent></FooterComponent>
    
  </footer>

</template>

<style lang="scss" >
@use './assets/scss/main.scss';

*{
  font-family: 'Roboto', sans-serif;
}
.container{
  width: 1140px;
  margin: 0 auto;
}

main{
  background-color: #1C1C1C;
  width: 100%;
  border: 1px solid black;

  h3{
    color: white;
    font-size: 48px;
    text-align: center;
  }
}



</style>
