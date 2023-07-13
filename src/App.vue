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
      <h3>Missing main content</h3>
    </div>
  </main>

  <footer>
    
    <section class="footer-links">
      <div class="container">
        <div class="link-elements">

          <div class="single-link-element">
            <img src="./assets/img/buy-comics-digital-comics.png" alt="">
            <h3>digital comics</h3>
          </div>

          <div class="single-link-element">
            <img src="./assets/img/buy-comics-digital-comics.png" alt="">
            <h3>digital comics</h3>
          </div>

          <div class="single-link-element">
            <img src="./assets/img/buy-comics-digital-comics.png" alt="">
            <h3>digital comics</h3>
          </div>

          <div class="single-link-element">
            <img src="./assets/img/buy-comics-digital-comics.png" alt="">
            <h3>digital comics</h3>
          </div>

          <div class="single-link-element">
            <img src="./assets/img/buy-comics-digital-comics.png" alt="">
            <h3>digital comics</h3>
          </div>

        </div>
      </div>
    </section>

    <section class="footer-info">
      <div class="container">
        <nav>
          <div>
          <h3>
            DC COMICS
          </h3>
          <ul>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
          </ul>

          <h3>
            DC COMICS
          </h3>
          <ul>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
          </ul>

          </div>

          <div>
          <h3>
            DC COMICS
          </h3>
          <ul>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
          </ul>
          </div>
          <div>
            <h3>
            DC COMICS
          </h3>
          <ul>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
            <li><a href="">Link</a></li>
          </ul>
          </div>
          
        </nav>
        <div id="bg-logo">
          <img src="./assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </section>

    <section class="footer-socials">
      <div class="container">
        <div>
          <button>Sign up now!</button>

          <div class="social-links">
            <h3>Follow Us</h3>
          
            <a href="">Link con Icon</a>

            <a href="">Link con Icon</a>

            <a href="">Link con Icon</a>

            <a href="">Link con Icon</a>
            
            <a href="">Link con Icon</a>

          </div>
         
        </div>
        
      </div>
    </section>
    
  </footer>

</template>

<style lang="scss" scoped>
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

footer{
  width: 100%;
  border: 1px solid black;
  
  section{
    

    &.footer-links{
      background-color: #2087EE;

      .link-elements{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
      }

      h3{
        display: inline-block;
        text-transform: uppercase;
        color: white;
        font-weight: 500;
        font-size: 13px;
      }
      .single-link-element{
        display: flex;
        align-items: center;

        img{
          scale: 50%;
        }
      }
    }
    &.footer-info{
      
      background-image: url('./assets/img/footer-bg.jpg');
      background-size: cover;
      background-repeat: no-repeat;
      
      overflow: hidden;
      .container{
        position: relative;
      }

      h3{
        color: white;
      }
      nav{
        display: flex;
        flex-wrap: wrap;

        > div{
          margin: 0 20px;
        }
      }
      #bg-logo{
        position: absolute;
        top: 0;
        right: 0;
        transform: translate(0, -20%);
        
      }
    }
    &.footer-socials{
      background-color: #303030;
      padding: 20px 0;

      .container > div{
        display: flex;
        align-items: center;
        justify-content: space-between;

        button{
          border: 2px solid #2087EE;
          padding: 10px 20px;
          text-transform: uppercase;
          background-color: rgba($color: #000000, $alpha: 0.0);
          color: white;

          &:hover{
            cursor: pointer;
            background-color: rgba($color: #2087EE, $alpha: 0.4);
          }
        }

        h3{
          text-transform: uppercase;
          color: #2087EE;
          padding-right: 20px;
        }
        a{
          color: #797979;
          text-decoration: none;
          margin: 0 10px;
        }
        .social-links{
          display: flex;
          align-items: center;
        }
      }
    }
  }
}

</style>
