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
    <div class="container">
      <nav>

        <div class="header-logo">
          <img src="./assets/img/dc-logo.png" alt="dc-logo">
        </div>
        <ul>

          <li>
            <a href=""> characters</a>
          </li>

          <li>
            <a href=""> comics</a>
          </li>

          <li>
            <a href=""> movies</a>
          </li>

          <li>
            <a href=""> tv</a>
          </li>

          <li>
            <a href=""> games</a>
          </li>

          <li>
            <a href=""> collectibles</a>
          </li>

          <li>
            <a href=""> videos</a>
          </li>

          <li>
            <a href=""> fans</a>
          </li>

          <li>
            <a href=""> news</a>
          </li>

          <li>
            <a href=""> shop</a>
          </li>


        </ul>
      </nav>
    </div>
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

.container{
  width: 1140px;
  margin: 0 auto;
}

header{
  width: 100%;
  margin: 20px 0;
    nav{
      display: flex;
      justify-content: space-between;
      
      ul{
        display: flex;
        align-items: center;
        text-transform: uppercase;
        margin: 0;

        li{
          margin: 0 5px;
          height: 100%;
          display: flex;
          align-items: center;
          padding: 0 10px;
          
          &:hover{
            border-bottom: 5px solid #2087EE;
          }

          &:hover a{
            color: #2087EE;
          }

          a{
            text-decoration: none;
            color: darkslategray;
            font-weight: 700;
            font-size: 12px;
          }
        }
      }
    }
    .header-logo{
      margin: 10px;
      scale: 80%;
    }
}

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
