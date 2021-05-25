<template>
  <div class="container">
    <h1>Hello Nuxters! 👋</h1>
    <p>
      This page is rendered on the <strong>{{ rendering }}</strong>
    </p>
    <p v-if="rendering === 'server'">
      First load or hard refresh is done on server side.
    </p>
    <p v-if="rendering === 'client'">Navigation is done on client side.</p>
    <ul>
      <li>Refresh the page for server side rendering.</li>
       <li>Refresh the page for server side rendering.</li>
      
    </ul>


    <NuxtLink to="/product">Product</NuxtLink>
     <NuxtLink to="/setting">Setting</NuxtLink>
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
