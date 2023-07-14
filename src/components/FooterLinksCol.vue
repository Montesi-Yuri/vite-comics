<script>

export default {
  data() {
    return {
    }
  },
  props:{
    singleInfo: Object,
    title: String,
  }
}

</script>


<template>
    <div :class="title">
        <h3>
            {{ title }}
        </h3>
        <ul>
            <li v-for="(link, i) in singleInfo.links" :key="i">
                <a href="">
                    {{ link }}
                </a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
h3{
    color: white;
}
a{
    color: #727274;
    text-decoration: none;
    font-size: 12px;
    font-weight: 600;
}

</style>