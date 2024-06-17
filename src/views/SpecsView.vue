<script>
import prods from '../assets/products.js'
export default {
    data () {
        return {
            prods: prods,
        }
    },
    computed: {
        product() {
            return this.prods.find(item => item.id === (this.$route.params.id.replace(':', '')));
        }
    }
}
</script>

<template>
    <div v-if="product" class="text-center grid place-content-center">
        <div class="flex justify-center">
            <img :src="product.img" alt="image" class="h-[200px]">
        </div>
        <h1 class="text-[30px] font-extrabold mb-3"> {{ product.name }}</h1>
        <p class="w-[400px] text-lg">{{ product.desc }}</p>
        <span class="text-start mt-6 font-semibold text-lg">Starts at <span class="text-red-500">{{ product.price }}</span></span>
    </div>
    <div v-else>
        <h1>Error 404. Product not found. Check the URL</h1>
    </div>
</template>

<style>
</style>