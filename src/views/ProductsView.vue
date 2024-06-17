<script>
import prods from '../assets/products.js'

export default {
    data () {
    return {
        products: prods
    }
    }
}
</script>

<template>
<div v-for="(item, index) in this.products" :key="index" class="mb-5 text-center">
    <h1 class="text-[30px] font-bold">{{ item.name }}</h1>
    <h2 class="text-[20px] font-semibold">{{ item.price }}</h2>
    <router-link :to="`/product/:${item.id}`" class="underline">View Specs</router-link>
</div>
</template>

<style>
</style>