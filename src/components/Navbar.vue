<script setup lang="ts">
import { useRouter, useRoute } from 'vue-router'
import { useCartStore } from '@/stores/cartStore'

const router = useRouter()
const route = useRoute()
const cartStore = useCartStore()

const navLinks = [
  { name: 'Home', path: 'home' },
  { name: 'Products', path: 'product' },
  { name: 'About', path: 'about' },
  { name: 'Contact', path: 'contact' },
  { name: 'Rating', path: 'rating' },
]

const isActive = (path: string) => {
  if (path === 'home') {
    return route.name === 'home'
  }
  return route.name === path
}

const goHome = () => {
  router.push({ name: 'home' })
}
</script>

<template>
  <nav
    class="fixed top-0 left-0 w-full z-50 bg-[#1a1613] border-b border-[rgba(200,169,106,0.2)] h-[80px]"
  >
    <div class="flex items-center justify-between h-full px-[120px]">
      <!-- Logo -->
      <div class="cursor-pointer hover:opacity-80 transition-opacity" @click="goHome">
        <h1 class="text-[24px] font-bold text-[#c8a96a] font-['Playfair_Display']">VELIXIER</h1>
      </div>

      <!-- Navigation Links -->
      <div class="flex items-center gap-8">
        <RouterLink
          v-for="link in navLinks"
          :key="link.path"
          :to="{ name: link.path }"
          class="font-['Inter'] text-[16px] transition-colors"
          :class="[isActive(link.path) ? 'text-[#c8a96a]' : 'text-[#d4c5b0] hover:text-[#c8a96a]']"
        >
          {{ link.name }}
        </RouterLink>
      </div>

      <!-- Cart Icon -->
      <RouterLink
        :to="{ name: 'cart' }"
        class="relative cursor-pointer hover:opacity-80 transition-opacity"
      >
        <svg class="w-6 h-6 text-[#c8a96a]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
        </svg>
        <span
          v-if="cartStore.itemCount > 0"
          class="absolute -top-2 -right-2 bg-[#c8a96a] text-[#1a1613] text-[12px] font-bold rounded-full w-5 h-5 flex items-center justify-center"
        >
          {{ cartStore.itemCount }}
        </span>
      </RouterLink>
    </div>
  </nav>
</template>

<style scoped>
a {
  text-decoration: none;
}
</style>
