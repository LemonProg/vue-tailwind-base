<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div>
      <nav class="flex justify-center gap-[50px] w-screen mt-5 mb-8">
        <RouterLink to="/" class="text-2xl hover:underline">Home</RouterLink>
        <RouterLink to="/products" class="text-2xl hover:underline">Products</RouterLink>
        <RouterLink to="/about" class="text-2xl hover:underline">About</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
</style>
