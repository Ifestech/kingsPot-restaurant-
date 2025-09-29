<template>
   <section class=" bg-[#065F46] text-white">
        <div class="Container">
          <nav class="flex justify-between items-center  ">
            <!-- Logo -->
             <div>
            <img src="../image/logo.jpg" alt="logo" class="h-16 w-16 rounded-full"/>
             </div>

            <!-- Nav Links (hidden on mobile) -->
            <div class="hidden md:flex gap-4 text-lg font-semibold">
            <RouterLink to="/" class="hover:underline hover:decoration-amber-600 hover:decoration-3 active:underline active:decoration-amber-400 active:decoration-2">Home</RouterLink>
            <RouterLink to="/menu" class="hover:underline hover:decoration-amber-600 hover:decoration-3 active:underline active:decoration-amber-400 active:decoration-2">Menu</RouterLink>
            <RouterLink to="/about" class="hover:underline hover:decoration-amber-600 hover:decoration-3 active:underline active:decoration-amber-400 active:decoration-2">About</RouterLink>
            <RouterLink to="/contact" class="hover:underline hover:decoration-amber-600 hover:decoration-3 active:underline active:decoration-amber-400 active:decoration-2">Contact-Us</RouterLink>
            </div>

            <!-- Right side: Login (desktop) + Hamburger + Cart -->
            <div class="flex items-center gap-4">
            <router-link to="/login" class="hidden md:inline px-4 py-2 rounded-lg font-bold bg-blue-500 hover:bg-blue-600 text-white">Login</router-link>

            <!-- Hamburger first on mobile -->
            <button @click="isOpen = !isOpen" class="md:hidden flex items-center p-2 text-white text-5xl font-bold ">
                <i v-if="!isOpen" class="bi bi-list"></i>
                <i v-else class="bi bi-x"></i>
            </button>

            <!-- Cart -->
            <RouterLink to="/cart" class="flex items-center justify-center w-12 h-12 rounded-full bg-blue-100 hover:bg-blue-200 text-blue-700">
                <i class="bi bi-cart3 text-xl"></i>
            </RouterLink>
            </div>
            </nav>

             <!-- Mobile dropdown menu -->
            <div v-if="isOpen" class="md:hidden flex flex-col gap-4 p-4 bg-white text-black text-lg font-semibold shadow">
            <RouterLink to="/" @click="isOpen=false" class="hover:underline hover:decoration-amber-600">Home</RouterLink>
            <RouterLink to="/menu" @click="isOpen=false" class="hover:underline hover:decoration-amber-600">Menu</RouterLink>
            <RouterLink to="/about" @click="isOpen=false" class="hover:underline hover:decoration-amber-600">About</RouterLink>
            <RouterLink to="/contact" @click="isOpen=false" class="hover:underline hover:decoration-amber-600">Contact-Us</RouterLink>
            <router-link to="/login" @click="isOpen=false" class="px-4 py-2 rounded-lg font-bold bg-blue-500 hover:bg-blue-600 text-white">Login</router-link>
            </div>
        </div> 
    </section>
</template>

<script setup>
import { ref } from "vue"
const isOpen = ref(false)
</script>

<style scoped>

</style>