<template>
    <div modal="true">
            <div v-if="visible" :data-modal="name"  class="modal">
                <div aria-modal="true" tabindex="-1" class="modal_mask" data-reach-dialog-content="true">
                   
                    <div class="modal_body">
                         <slot :payload="payload"/>
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
<style  scoped>
.modal{

  position: fixed;

  top: 50%;

  left: 50%;

  transform: translate(-50%, -50%);

  width: 300px;

  height: 200px;

  z-index: 1000;


  border-radius: 2px;

  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);


}
</style>