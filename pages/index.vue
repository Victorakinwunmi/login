<template>
  <div>

    <div class="flex w-full">

      <div class="bg-black hidden lg:block lg:w-5/12"> 

        <LeftDisplay v-for="item in display" :key="item.id"
           :pic="item.pic"
           :logo="item.logo"
        />

      </div>
      
      <div class="w-full md:mx-10 lg:w-7/12">
         <LoginForm  v-for="item in login" :key="item.id"

           :title="item.title"
           :subtitle="item.subtitle"
           :desc="item.desc"
          
           

         />

        <div class="mx-10 grid grid-cols-1 xl:grid-cols-2 grid-gap-2 xl:mx-32">

         
            <div class="mt-8 ">

                <div  class="mb-2 font-semibold text-gray-500 text-lg">First name</div>
                
                <input type="text" class="border-2 border-gray-300 w-full p-1 outline-none rounded focus:border-blue-300">

            </div>

            <div class="mt-8 ">

                <div class="mb-2 mx-2 font-semibold text-gray-500 text-lg">Last Name</div>

                <input type="text" class="border-2 border-gray-300 w-full p-1 lg:mx-2 outline-none rounded focus:border-blue-300 ">

            </div>

            <div class="mt-8 ">

                <div  class="mb-2 font-semibold text-gray-500 text-lg">Phone number</div>

                <input type="number" class="border-2 border-gray-300 w-full p-1 outline-none rounded focus:border-blue-300 ">

            </div>

            <div class="mt-8 ">

                <div  class="mb-2 mx-2 font-semibold text-gray-500 text-lg">Email</div>

                <input type="email" class="border-2 border-gray-300 w-full p-1 lg:mx-2 outline-none rounded focus:border-blue-300">

            </div>

            <div class="mt-8 ">

                <div  class="mb-2 font-semibold text-gray-500 text-lg">Password</div>

                <input type="password" class="border-2 border-gray-300 w-full p-1 outline-none rounded focus:border-blue-300">

            </div>

            <div class="mt-8 ">

                <div  class="mb-2 mx-2 font-semibold text-gray-500 text-lg">Confirm password</div>

                <input type="password" class="border-2 border-gray-300 w-full lg:mx-2 p-1 outline-none rounded focus:border-blue-300">

            </div>

        </div>

        <div class="flex mx-10 xl:mx-32 mt-10">
          <input type="checkbox">
          <h1 class="mx-2 text-gray-500 font-semibold">Yes i want to recieve lottery display email</h1>
        </div>

        <div class="flex mx-10 xl:mx-32 mt-6">
          <input type="checkbox">
          <h1 class="mx-2 text-gray-500 font-semibold">I agree to the <span class="font-bold text-blue-500">Term, privacy policy</span> and <span class="font-bold text-blue-500">Fees</span></h1>
        </div>

        <div class="mx-10 xl:mx-32 mb-6 mt-10">
          <nuxt-link to="dashboard" class="border text-white bg-gray-500 mt-10 p-4 px-16 rounded-2xl hover:bg-black">Create Account</nuxt-link>
          <h1 class="mt-8 mx-2 md:mx-0 font-bold text-gray-500">Already have an account? <span class="text-blue-500 font-bold">Log in</span></h1>
        </div>
         
      </div>

    </div>

  
  </div>

</template>

<script>
export default {
    data() {
        return {
             
            login: [
              {
                title:"Register",
                subtitle:"Mange all your lottery efficiently",
                desc:`Let's get you all set up so you can
                      verify your personal account and begin
                      setting up your profile
                     `,
               
              }

            
            ],

            display: [
              {
               pic: require('@/assets/tech/background.jpg'),
               logo: require('@/assets/tech/logo.png')
              },
            ]
        };
    },
   
    
}
</script>

<style>

</style>
