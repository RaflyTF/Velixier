<script setup lang="ts">
import { useRouter } from 'vue-router'
import { useCartStore } from '@/stores/cartStore'
import JPGLeMale from '@/assets/JPGLeMale.png'
import KingSCE from '@/assets/KingSCE.png'
import SharafBlend from '@/assets/SharafBlend.png'
import CalvinKlein from '@/assets/CalvinKlein.png'

const router = useRouter()
const cartStore = useCartStore()

const products = [
  { id: '1', image: JPGLeMale, name: 'JPG Le Male EDP', price: 2280000 },
  { id: '2', image: KingSCE, name: 'King SCE Collection', price: 750000 },
  { id: '3', image: SharafBlend, name: 'Sharaf Blend Zimaya', price: 600000 },
  { id: '4', image: CalvinKlein, name: 'Calvin Klein One', price: 1200000 },
]

const addToCart = (product: (typeof products)[0]) => {
  cartStore.addToCart({
    id: product.id,
    name: product.name,
    price: product.price,
    image: product.image,
  })
  router.push({ name: 'cart' })
}
</script>

<template>
  <div class="relative flex flex-col items-center px-[120px] py-16 w-full bg-[#0d0c0a]">
    <div class="flex flex-col gap-4 items-center mb-12">
      <div
        class="flex flex-col font-['Playfair_Display'] font-bold justify-center text-[40px] text-[#c8a96a] text-center"
      >
        <p>Best Sellers</p>
      </div>
      <div
        class="flex flex-col font-['Inter'] justify-center text-[18px] text-[#d4c5b0] text-center max-w-[600px]"
      >
        <p>Discover our most beloved fragrances, chosen by connoisseurs worldwide</p>
      </div>
    </div>

    <!-- Product Cards - Grid 2x2 -->
    <div class="grid grid-cols-2 gap-x-[60px] gap-y-[50px] w-full max-w-[1400px]">
      <div
        v-for="product in products"
        :key="product.id"
        class="bg-[#1a1613] h-[500px] overflow-clip relative rounded-[24px] shadow-[0px_8px_24px_rgba(0,0,0,0.4)] w-full cursor-pointer hover:scale-105 hover:shadow-[0px_12px_32px_rgba(200,169,106,0.3)] transition-all duration-300 border border-[rgba(200,169,106,0.2)]"
      >
        <div class="h-[280px] w-full overflow-hidden">
          <img
            :src="product.image"
            :alt="product.name"
            class="w-full h-full object-cover hover:scale-110 transition-transform duration-500"
          />
        </div>
        <div class="flex flex-col px-[30px] pt-[30px] pb-[24px] h-[220px]">
          <p
            class="font-['Playfair_Display'] font-semibold text-[20px] text-[#c8a96a] line-clamp-2 min-h-[56px]"
          >
            {{ product.name }}
          </p>
          <p class="font-['Inter'] font-medium text-[18px] text-[#d4c5b0] mt-[16px]">
            Rp. {{ product.price.toLocaleString('id-ID') }}
          </p>
          <button
            @click="addToCart(product)"
            class="bg-[#c8a96a] hover:bg-[#b89960] box-border flex gap-[10px] items-center justify-center p-[14px] rounded-[12px] transition-all duration-300 hover:shadow-lg mt-auto font-['Inter'] font-medium text-[15px] text-[#1a1613]"
          >
            Add to cart
            <svg class="w-5 h-5" fill="#1a1613" viewBox="0 0 24 24">
              <path
                d="M7 4V2m10 2v-2m-3 2h-4a3 3 0 0 0-3 3v10a3 3 0 0 0 3 3h4a3 3 0 0 0 3-3V6a3 3 0 0 0-3-3z"
                stroke="#1a1613"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                fill="none"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
