<script setup lang="ts">
import { useRouter } from 'vue-router'
import citrusNote from '@/assets/CitrusNote.png'
import floralNote from '@/assets/FloralNote.png'
import woodyNote from '@/assets/WoodyNote.png'

const router = useRouter()

const notes = [
  { image: citrusNote, label: 'Citrus Note' },
  { image: floralNote, label: 'Floral Note' },
  { image: woodyNote, label: 'Woody Note' },
]

const navigateToProducts = () => {
  router.push({ name: 'product' })
}
</script>

<template>
  <div class="relative flex flex-col gap-[42px] items-center px-[120px] py-20 w-full bg-[#0d0c0a]">
    <div
      class="flex flex-col font-['Playfair_Display'] font-bold justify-center text-[40px] text-[#c8a96a] text-center w-full"
    >
      <p>Best Note For Fragrance</p>
    </div>
    <div class="flex gap-[50px] items-center w-full justify-center flex-wrap">
      <div
        v-for="note in notes"
        :key="note.label"
        class="relative flex flex-col gap-[10px] items-center justify-center rounded-[20px] h-[280px] w-[280px] cursor-pointer hover:scale-105 transition-all duration-300 shadow-xl hover:shadow-2xl overflow-hidden group"
        @click="navigateToProducts"
      >
        <img
          :src="note.image"
          :alt="note.label"
          class="absolute inset-0 max-w-none object-center object-cover pointer-events-none rounded-[20px] size-full group-hover:scale-110 transition-transform duration-500"
        />
        <div
          class="absolute inset-0 bg-gradient-to-b from-[rgba(0,0,0,0.3)] to-[rgba(0,0,0,0.6)] group-hover:from-[rgba(0,0,0,0.4)] group-hover:to-[rgba(0,0,0,0.7)] transition-all duration-300"
        />
        <div
          class="relative flex flex-col font-['Playfair_Display'] font-bold justify-center text-[28px] text-center text-white z-10"
        >
          <p>{{ note.label }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
