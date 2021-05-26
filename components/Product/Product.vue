<template>
        <div class="list-item" >
          <nuxt-link :to="`/product/${id}`" >
              <div class="item">
                <img :src="thuml" alt="">
                <h3>{{ name}}</h3>
                <p>{{ desc }}</p>
              </div>
          </nuxt-link>
        </div>
</template>
<script>

export default {
    props:{
        id:{
            type:Number,
            required: true
        },
        name:{
            type:String,
            required:true
        },
        desc:{
            type:String,
            default:''
        },
        thuml:{
            type:String,
            required:true
        }
    }
}
</script>