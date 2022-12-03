<template>
  <div class="block lg:flex">
    <SidebarContainer>
      <template #hamburgermenuopen>
        <button class="">
          <img :src="require('@/assets/icons/Menu.png')" class="w-8 m-0 p-0" />
        </button>
      </template>

      <template #hamburgermenuclose>
        <button class="">
          <img :src="require('@/assets/icons/Close.png')" class="w-8 m-0 p-0" />
        </button>
      </template>

      <template #logo>
        <SidebarLogo />
      </template>

      <template #menu>
        <SidebarMenu path="./dashboard">
          <div><SharedIcons icon_name="icon1" /></div>
          <div>Home</div>
        </SidebarMenu>

        <SidebarMenu path="./classes">
          <div><SharedIcons icon_name="icon2" /></div>
          <div>Classes</div>
        </SidebarMenu>

        <SidebarMenu path="./payments">
          <div><SharedIcons icon_name="icon3" /></div>
          <div>Payments</div>
        </SidebarMenu>

        <SidebarMenu path="./tools">
          <div><SharedIcons icon_name="icon4" /></div>
          <div>Tools</div>
        </SidebarMenu>
      </template>

      <template #logout>
        <div><SidebarLogout /></div>
      </template>
    </SidebarContainer>

    <div class="w-full p-6 lg:px-32 xl:px-40">
      <div class="">
        <HeaderContent>
          <template #text>
            <div>Hello,Victor</div>
          </template>

          <template #button>
            <button
              class="
                font-bold
                text-2xl
                border
                bg-black
                text-white
                rounded-full
                py-4
                px-6
              "
            >
              Create a class
            </button>
          </template>
        </HeaderContent>
      </div>

      <div
        class="
          grid grid-cols-1
          md:grid-cols-2
          lg:grid-cols-2
          xl:grid-cols-4
          mt-16
          gap-6
        "
      >
        <div class="">
          <CardContainer>
            <template #icon>
              <div class="border bg-black h-20 w-20 rounded-full">
                 <img
                  :src="require('@/assets/icons/Book.png')"
                  class="w-8 mt-5 mx-auto"
                />
              </div>
            </template>

            <template #details>
              <div class="font-semibold text-xl">Total bookings</div>

              <div class="font-bold text-3xl">276</div>
            </template>
          </CardContainer>
        </div>

        <div class="">
          <CardContainer>
            <template #icon>
              <div class="border bg-black h-20 w-20 rounded-full">
                <img
                  :src="require('@/assets/icons/Classes.png')"
                  class="w-8 mt-5 mx-auto"
                />
              </div>
            </template>

            <template #details>
              <div class="font-semibold text-xl">Total Classes</div>

              <div class="font-bold text-3xl">8</div>
            </template>
          </CardContainer>
        </div>

        <div>
          <CardContainer>
            <template #icon>
              <div class="border bg-black h-20 w-20 rounded-full">
                <img
                  :src="require('@/assets/icons/Dollar.png')"
                  class="w-10 mt-4 mx-auto"
                />
              </div>
            </template>

            <template #details>
              <div class="font-semibold text-xl">Total Earnings</div>

              <div class="font-bold text-3xl">$15,000</div>
            </template>
          </CardContainer>
        </div>
      </div>

      <div class="flex justify-between mt-16">
        <div class="">
          <h1 class="text-black font-bold text-2xl">Recent classes</h1>
        </div>

        <div class="font-semibold text-gray-500">
          <a href="https://www.vicky.com">View all</a>
        </div>
      </div>

      <div
        class="
          grid grid-cols-1
          md:grid-cols-2
          lg:grid-cols-3
          xl:grid-cols-4
          gap-6
        "
      >
        <PurchaseContainer1
          v-for="item in card"
          :key="item.id"
          :price="item.price"
          :title="item.title"
          :desc="item.desc"
          :btn="item.btn"
          :rating="item.rating"
          :reviewcount="item.reviewcount"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      card: [
        {
          id: 1,
          price: "$150",
          title: "Shopify masterclass",
          desc: "Bookings - 45",
          btn: "View details",
          rating:4,
          reviewcount:"Based 34 reviews"
        },

        {
          id: 2,
          price: "$10",
          title: "How to start a YouTube channel",
          desc: "Bookings - 25",
          btn: "View details",
          rating:5,
          reviewcount:"Based 14 reviews"
        },

        {
          id: 3,
          price: "Free",
          title: "Introduction to UI/UX design",
          desc: "Bookings - 30",
          btn: "View details",
          rating:3,
          reviewcount:"Based 50 reviews"
        },

        {
          id: 4,
          price: "$100",
          title: "How to manage your social media account",
          desc: "Booking - 45",
          btn: "View details",
          rating:4,
          reviewcount:"Based 30 reviews"
        },
      ],
    };
  },
};
</script>

<style>
</style>