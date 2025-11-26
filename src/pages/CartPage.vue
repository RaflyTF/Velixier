<template>
  <div class="min-h-screen bg-[#0d0c0a] px-[120px] py-20">
    <div class="max-w-[1400px] mx-auto">
      <h1 class="font-['Playfair_Display'] font-bold text-[48px] text-[#c8a96a] mb-8">
        Shopping Cart
      </h1>
      <div v-if="cartStore.items.length === 0" class="font-['Inter'] text-[16px] text-[#d4c5b0]">
        <p>Your cart is empty</p>
        <RouterLink to="/product" class="text-[#c8a96a] hover:text-[#b89960] transition-colors mt-4 inline-block">
          Continue Shopping
        </RouterLink>
      </div>
      <div v-else>
        <div class="space-y-4">
          <div
            v-for="item in cartStore.items"
            :key="item.id"
            class="bg-[#1a1613] p-6 rounded-lg flex justify-between items-center border border-[rgba(200,169,106,0.2)]"
          >
            <div class="flex items-center gap-4">
              <img :src="item.image" :alt="item.name" class="w-20 h-20 object-cover rounded" />
              <div>
                <p class="text-[#c8a96a] font-bold">{{ item.name }}</p>
                <p class="text-[#d4c5b0]">Rp. {{ item.price.toLocaleString('id-ID') }}</p>
              </div>
            </div>
            <div class="flex items-center gap-4">
              <input
                v-model.number="item.quantity"
                type="number"
                min="1"
                class="w-16 px-2 py-1 bg-[#0d0c0a] text-[#d4c5b0] border border-[rgba(200,169,106,0.2)] rounded"
              />
              <button
                @click="cartStore.removeFromCart(item.id)"
                class="bg-red-600 hover:bg-red-700 text-white px-4 py-2 rounded transition-colors"
              >
                Remove
              </button>
            </div>
          </div>
        </div>
        <div class="mt-8 text-right">
          <p class="text-[#d4c5b0] text-lg mb-4">
            Total: <span class="text-[#c8a96a] font-bold">Rp. {{ cartStore.totalPrice.toLocaleString('id-ID') }}</span>
          </p>
          <button class="bg-[#c8a96a] hover:bg-[#b89960] text-[#1a1613] px-12 py-3 rounded-lg transition-all">
            Checkout
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { useCartStore } from '@/stores/cartStore'

const cartStore = useCartStore()
</script>
