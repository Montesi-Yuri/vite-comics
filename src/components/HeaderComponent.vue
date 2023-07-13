<script>

export default {
  data() {
    return {
      navLinks:[
        {name: 'characters'},
        {name: 'comics'},
        {name: 'movies'},
        {name: 'tv'},
        {name: 'games'},
        {name: 'collectibles'},
        {name: 'videos'},
        {name: 'fans'},
        {name: 'news'},
        {name: 'shop'},
      ]
    }
  },
  
}

</script>

<template>
   <div class="container">
      <nav>
        <div class="header-logo">
          <img src="../assets/img/dc-logo.png" alt="dc-logo">
        </div>
        <ul>
          <li v-for="singleLink in navLinks" :key="singleLink">
            <a href="">{{singleLink.name}}</a>
          </li>
        </ul>
      </nav>
    </div>
</template>

<style lang="scss" scoped>
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
</style>
