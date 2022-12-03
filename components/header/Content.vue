<template>
  <div class="block lg:flex justify-between items-center mt-16">
    <div class="font-bold text-4xl">
      <slot name="text"></slot>
    </div>

    <div class=" mt-6">
      <a href="https://www.btn.com">
        <slot name="button"></slot>
      </a>
     
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>