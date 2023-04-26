<script>

import Header from '@/components/Header.vue'


export default {
  name:'App',
  components:{
    Header
  },
  data() {
    return {
      title: 'Ciao Vue - Vite'
    }
  },
}
</script>

<template>

  <Header />

  <h1>{{ title }}</h1>
</template>


<style scoped>
  h1{
    color: yellow;
  }


</style>