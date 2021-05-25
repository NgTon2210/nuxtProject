<template>
  <div class="container">
    <div class="row banner">

    </div>
    <h1>Hello Nuxters! 👋</h1>
    <p>
      This page is rendered on the <strong>{{ rendering }}</strong>
    </p>
    <p v-if="rendering === 'server'">
      First load or hard refresh is done on server side.
    </p>
    <p v-if="rendering === 'client'">Navigation is done on client side.</p>
  


    
  </div>
</template>
<script>
export default {
  data(){
    return{
      name:"nguyen ton"
    }
  },
  asyncData() {
    return {
      rendering: process.server ? 'server' : 'client'
    }
  }
}
</script>
<style scoped>
  .nuxt-link-active{
    font-weight: 700;
    color: wheat;
  }
  .banner{
    height: 300px;
    background-image: url('~assets/image/images.jpg');
    background-size: cover;
    background-repeat: no-repeat;
  }
</style>
