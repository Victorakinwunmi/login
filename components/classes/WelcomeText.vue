<template>
  <div class="mt-16 rounded-md shadow-md lg:mt-0 bg-gray-200 p-4 flex justify-between items-center">
    <div class="">
      <h1 class="font-bold text-5xl mb-6">Welcome</h1>
      <p>These are your classes below</p>
    </div>
    <div>
      <div class="block lg:hidden h-20 w-20 rounded-full overflow-hidden border-2 border-white">
        <img :src="require('@/assets/tech/dp.jpg')" class="full h-full object-cover">
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>