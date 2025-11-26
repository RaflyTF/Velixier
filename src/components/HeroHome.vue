<script setup lang="ts">
import { useRouter } from 'vue-router'
import heroImage from '@/assets/HeroHome.webp'

const router = useRouter()

const navigateToProducts = () => {
  router.push({ name: 'product' })
}
</script>

<template>
  <div class="relative h-[700px] w-full">
    <img
      :src="heroImage"
      alt="Hero Banner"
      class="absolute inset-0 max-w-none object-center object-cover pointer-events-none size-full"
    />
    <div class="absolute inset-0 bg-gradient-to-b from-[rgba(0,0,0,0.6)] to-[rgba(0,0,0,0.4)]" />

    <!-- Hero Content -->
    <div class="absolute inset-0 flex flex-col items-center justify-center px-[120px]">
      <div class="text-center max-w-[900px] space-y-6">
        <h1 class="font-['Playfair_Display'] font-bold text-[64px] leading-[1.1] text-[#c8a96a]">
          Discover Your Signature Scent
        </h1>
        <p class="font-['Inter'] text-[20px] leading-[1.6] text-[#f5f1e8]">
          Experience luxury fragrances crafted with artisanal precision. Each bottle tells a story
          of elegance, sophistication, and timeless beauty.
        </p>
        <button
          @click="navigateToProducts"
          class="bg-[#c8a96a] hover:bg-[#b89960] text-[#1a1613] px-12 py-4 rounded-full transition-all duration-300 mt-8 shadow-lg hover:shadow-xl hover:scale-105 font-['Inter'] font-semibold text-[16px]"
        >
          Explore Collection
        </button>
      </div>
    </div>
  </div>
</template>
