<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import MainComponent from './components/MainComponent.vue';

export default {
  data() {
    return {
    }
  },
  components:{
    HeaderComponent,
    MainComponent,
    FooterComponent,

  }
}
</script>

<template>
  <header>
   <HeaderComponent></HeaderComponent>
  </header>

  <main>
    <MainComponent></MainComponent>
  </main>

  <footer>
    <FooterComponent></FooterComponent>
  </footer>
</template>

<style lang="scss" >
@use './assets/scss/main.scss' as *;

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
	padding-bottom: 50px;
}
.single-series {
	margin: 10px;
	width: 180px;
	cursor: pointer;

    &:hover{
      opacity: 0.3;
    }
}
</style>
