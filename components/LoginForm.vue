<template>
  <div>
     <div class="mx-10 xl:mx-32 mt-16">

        <div class="">
           <h1 class="font-bold text-3xl text-black">{{title}}</h1> 
        </div>

        <div class="mt-16 w-full">
           <h1 class="font-semibold text-xl text-current">{{subtitle}}</h1>
        </div>

        <div class="mt-5 w-full md:w-8/12">
            <h1 class="text-gray-500 font-medium">{{desc}}</h1>
        </div>

    
         

     </div>
  




  </div>
</template>

<script>
export default {
    props: {
       title: String,
       subtitle: String,
       desc: String,
       password:Number,
    },
}
</script>

<style>

</style>