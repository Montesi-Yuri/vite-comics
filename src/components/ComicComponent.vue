<script>
export default {
  data() {
    return {
    }
  },
  props:{
    src: String,
    name: String
  }
}

</script>

<template>

   
    <div>
        <img :src="src" :alt="name">
    </div>
    <h3>{{ name }}</h3>
    

</template>

<style lang="scss" scoped>

div{
    display: flex;
    align-items: center;
    justify-content: center;
    img{
        width: 150px;
        height: 200px;
        object-fit: cover;
    }
}
    
h3{
    color: white;
    font-weight: 500;
    text-align: center;
    word-break: break-word;
}

</style>