<template>
    <div modal="true">
        <div>
            <div :data-modal="name" v-if="visible" class="modal">
                <div aria-modal="true" tabindex="-1" class="modal_mask">
                    <div class="modal_body">
                        <slot :payload="payload"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import VModal from "./handle"
export default {
   props:{
       name:{
           type: String,
           required: true
       }
   },
   data(){
       return{
           payload:null,
           visible: false
       }
   },
    beforeMount(){
       VModal.EventBus.$on('open', params =>{
           if(this.name === params.name){
               this.open(params)
           }
       }),
         VModal.EventBus.$on('close', params =>{
           if(this.name === params.name){
               this.close(params)
           }
       })
   },
   methods:{
       close(params){
           this.visible = false
       },
       open(params){
           this.visible = true
       }
   }
  
}
</script>