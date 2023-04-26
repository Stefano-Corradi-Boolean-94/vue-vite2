
<script>
export default {
  name:'Header',
  data() {
    return {
      logo:'LOGO',
      image: 'vue.svg'
    }
  },  
  methods:{
    // funzione per gestire le immagini dinamicamente 
    getImage(img){
      return new URL(`../assets/${img}`, import.meta.url).href
    }
  }
}
</script>


<template>
  <nav>
    <ul>
      <li><a href="#">{{ logo }} 
        <!-- immagine da assets  -->
        <img src="../assets/vue.svg" alt="assets"> 
        <!-- immagine da public com percorso assoluto partendo da public  -->
        <img src="/vite.svg" alt="public"> 
        <!-- immagine dinamica  -->
        <img :src="getImage(image)" alt="dinamica"> 
        </a></li>
      <li><a href="#">link</a></li>
      <li><a href="#">link</a></li>
      <li><a href="#">link</a></li>
    </ul>
  </nav>
  
</template>

<style scoped>
    nav li{
      list-style: none;
      display: inline-block;
      margin: 0 20px;
    }
</style>