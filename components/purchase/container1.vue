<template>
  <div
    class="mt-16 border border-white bg-white shadow-2xl h-4/5 rounded-3xl p-5"
  >
    <div class="flex justify-between items-center">
      <div>
        <div class="text-black font-bold text-3xl">{{ price }}</div>
      </div>

      <div class="flex">
        <div class="border rounded-full bg-black w-2 h-2"></div>
        <div class="border rounded-full bg-black w-2 h-2"></div>
        <div class="border rounded-full bg-black w-2 h-2"></div>
      </div>
    </div>

    <div class="mt-10">
      <h1 class="text-gray-600 font-semibold leading-tight truncate">
        {{ title }}
      </h1>
    </div>

    <div class="border border-gray-400 mt-8"></div>
    <div class="flex lg:block xl:flex justify-between items-center mt-10">
      <div>
        <h1 class="font-bold text-xl">{{ desc }}</h1>
      </div>

      <button
        class="
          border
          bg-black
          text-gray-300
          font-semibold
          p-3
          text-center
          rounded-full
          flex
          items-center
          lg:mt-5
          xl:mt-0
        "
        @click=" handleShowWhenClicked(price)"
      >
        <div class="w-full">
          {{ btn }}
        </div>
        <div>
          <img :src="require('@/assets/icons/Arrow.png')" class="w-5 mx-2" />
        </div>
      </button>
    </div>

    <div class="flex mt-4 mb-4">
      <svg
        v-for="i in 5" :key="i"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        class="h-5 w-5 fill-current"
        :class="i <= rating ? 'text-black':'text-gray-400'"
        viewBox="0 0 50 50"
        version="1.1"
      >
        <g id="surface1">
          <path
            style="
              stroke: none;
              fill-rule: nonzero;
              fill: rgb(0%, 0%, 0%);
              fill-opacity: 1;
            "
            d="M 39.695313 47.226563 C 39.511719 47.226563 39.324219 47.175781 39.164063 47.070313 L 25 38.179688 L 10.835938 47.070313 C 10.492188 47.289063 10.046875 47.273438 9.71875 47.035156 C 9.386719 46.796875 9.234375 46.378906 9.335938 45.980469 L 13.414063 29.765625 L 0.582031 19.042969 C 0.269531 18.78125 0.148438 18.355469 0.273438 17.964844 C 0.398438 17.578125 0.75 17.304688 1.15625 17.277344 L 17.839844 16.144531 L 24.070313 0.628906 C 24.222656 0.25 24.59375 0 25 0 C 25.40625 0 25.777344 0.25 25.929688 0.628906 L 32.160156 16.144531 L 48.84375 17.277344 C 49.25 17.304688 49.601563 17.578125 49.726563 17.964844 C 49.851563 18.355469 49.730469 18.777344 49.417969 19.042969 L 36.585938 29.765625 L 40.664063 45.980469 C 40.765625 46.378906 40.613281 46.792969 40.28125 47.035156 C 40.109375 47.160156 39.902344 47.226563 39.695313 47.226563 Z "
          />
        </g>
      </svg>

      <span class="mx-5">({{reviewcount}})</span>
    </div>

  </div>
</template>

<script>
export default {
  props: {
    price: String,
    title: String,
    desc: String,
    btn: String,
    rating: Number,
    reviewcount: String,
  },
   
  methods: {
        handleShowWhenClicked(price){

            let my_data = {
                price: price,
            }
            
            this.$emit("showButtonClicked", my_data)
        }
    }
};
</script>

<style>
</style>