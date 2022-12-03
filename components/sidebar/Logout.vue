<template>
  <div class="mb-10">
    <a href="https://www.adex.com">
      <img :src="path ? path : require('@/assets/icons/Exit.png')" class="mx-auto" />
    </a>
   
  </div>
</template>


<script>
export default {
   props :{
     path:{
       type: String,
       default:''
     } 
   }
}
</script>

<style>

</style>