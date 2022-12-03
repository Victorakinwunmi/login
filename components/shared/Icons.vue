<template>
  <img v-if="icon_name == 'icon1'" :src="require('@/assets/icons/Dog_House.png')" class="mx-auto"/>
  <img v-else-if="icon_name == 'icon2'" :src="require('@/assets/icons/Classes.png')" class="mx-auto"/>
  <img v-else-if="icon_name == 'icon3'" :src="require('@/assets/icons/Payments.png')" class="mx-auto" />
  <img v-else-if="icon_name == 'icon4'" :src="require('@/assets/icons/Tools.png')" class="mx-auto" />
  <img v-else :src="require('@/assets/tech/logo.png')"  class="w-20"/>
</template>

<script>
export default {
    props: {
        icon_name: {
            type: String,
            default: ''
        }
    }

};
</script>

<style>
</style>