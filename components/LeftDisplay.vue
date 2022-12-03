<template>

  <div>
      

    <div>
        <div class=" bg-no-repeat bg-cover bg-center h-screen"
            :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' + pic + ')' }">
            <div class=" p-10 text-white bg-black bg-opacity-60 w-full h-screen ">
                
                <div class="w-full p-10">
                   <img :src="logo" class="w-32">
                </div>

                <div class="mt-48 p-10">
                    <h1 class="font-bold text-3xl leading-normal lg:text-5xl">A few clicks away from creating your lottery display</h1>
                </div>

            </div>


        </div>
    </div>

  
  </div>

</template>

<script>
export default {
  props: {
     pic: String,
     logo: String,
  }
}
</script>

<style>

</style>