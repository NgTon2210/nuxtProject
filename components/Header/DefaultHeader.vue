<template>
    <div class="header ">
    
        <ul class="container">
            <li> <NuxtLink to="/">Home</NuxtLink></li>
            <li><a href="">About</a></li>
            <li> <NuxtLink to="/product">Product</NuxtLink></li>
             <li><NuxtLink to="/setting">Setting</NuxtLink></li>
        </ul>
    </div>
</template>
<style scoped>
    .header{
        padding:20px 0px;
        background: rgb(172, 166, 166);
    }
    ul{
        display: flex;
        list-style: none;
    }
    li{
        padding: 0px 15px;
    }
    a{
        color: black;
        font-weight: 300;
        text-decoration: none;
      
    }
     .nuxt-link-active{
    font-weight: 700;
    color: wheat;
  }
</style>