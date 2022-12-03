<template>
    <div class="my-8 text-white p-2 text-center hover:text-gray-400 hover:bg-gray-700">
        <a :href="path"><slot /></a>
    </div>
  
</template>

<script>
export default {
    props: {
        path: String,
    }

}
</script>

<style>

</style>