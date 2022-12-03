<template>
  <div class="flex justify-start gap-6 items-center rounded-3xl w-full h-auto shadow-xl px-6 py-8 lg:py-12 border border-gray-200">

     <div class="">
        <slot name="icon"></slot>
     </div>

     <div>
        <slot name="details"></slot>
     </div>


     

  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>