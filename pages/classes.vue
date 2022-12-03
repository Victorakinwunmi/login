<template>
<div>
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
      <ClassesWelcomeText />

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
         @showButtonClicked="showPrice"
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
          rating: 4,
          reviewcount: "Based 34 reviews",
        },

        {
          id: 2,
          price: "$10",
          title: "How to start a YouTube channel",
          desc: "Bookings - 25",
          btn: "View details",
          rating: 5,
          reviewcount: "Based 14 reviews",
        },

        {
          id: 3,
          price: "Free",
          title: "Introduction to UI/UX design",
          desc: "Bookings - 30",
          btn: "View details",
          rating: 3,
          reviewcount: "Based 50 reviews",
        },

        {
          id: 4,
          price: "$100",
          title: "How to manage your social media account",
          desc: "Booking - 45",
          btn: "View details",
          rating: 4,
          reviewcount: "Based 30 reviews",
        },
        {
          id: 5,
          price: "$75",
          title: "How to create and promote your social media account",
          desc: "Booking - 6",
          btn: "View details",
          rating: 2,
          reviewcount: "Based 10 reviews",
        },
        {
          id: 6,
          price: "$55",
          title: "how to create an app using kotlin",
          desc: "Booking - 35",
          btn: "View details",
          rating: 5,
          reviewcount: "Based 40 reviews",
        },
        {
          id: 7,
          price: "$80",
          title: "Get more followers on tiktok",
          desc: "Booking - 70",
          btn: "View details",
          rating: 4,
          reviewcount: "Based 15 reviews",
        },
        {
          id: 7,
          price: "$45",
          title: "How to make facebook ads",
          desc: "Booking - 20",
          btn: "View details",
          rating: 3,
          reviewcount: "Based 37 reviews",
        },
      ],
    };
  },
  methods: {
    showPrice(my_data) {
      alert("The price is"+ " " + my_data.price);
    },
  },
};
</script>

<style>

</style>