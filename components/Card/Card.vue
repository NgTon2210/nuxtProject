<template>
     <div class="col-lg-3">
          <nuxt-link to="" class="product-item">
            <img class="img-fluid"
              :src="thuml"
              alt="">
            <div class="name">{{ name}}</div>
          </nuxt-link>
        </div>
</template>
<script>
    export default {
        props:{
           thuml:{
               type:String,
               required:true
           },
           name:{
               type:String,
               required:true
           }
        }
    }
</script>