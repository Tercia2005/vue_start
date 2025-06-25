<template>
    <div class="hrrequest">
      <h1>HR REQUESTS</h1>
      <HRlist />
    </div>
</template>

<script>
import HRlist from '@/components/HRlist.vue';



export default{
   components: {
    HRlist,
  

   },

   data(){
    return {
        requests: [
            
        ]
    }
   }
}


</script>

<style>
  h1{
    text-align: center;
    
  }
</style>