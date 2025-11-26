<template>
  <div class="bg-[#1a1613] box-border content-stretch flex flex-col gap-[48px] items-start pb-0 pt-[64px] px-[120px] w-full" data-name="AppFooter">
    <div class="gap-[96px] grid grid-cols-[repeat(4,_minmax(0px,_1fr))] w-full">
      <!-- Brand -->
      <div class="content-stretch flex flex-col gap-[16px] items-start relative shrink-0">
        <p class="font-['Playfair_Display:Regular',_sans-serif] font-normal leading-[24px] text-[16px] text-[#c8a96a]">VELIXIER</p>
        <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[22.75px] not-italic text-[14px] text-[#d4c5b0] max-w-[330px]">
          Crafting luxury fragrances with artisanal precision and timeless elegance.
        </p>
      </div>

      <!-- Quick Links -->
      <div class="content-stretch flex flex-col gap-[16px] items-start relative shrink-0">
        <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[24px] not-italic text-[16px] text-[#c8a96a]">Quick Links</p>
        <div class="space-y-2">
          <router-link
            to="/product"
            class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-[#d4c5b0] cursor-pointer hover:text-[#c8a96a] transition-colors block"
          >
            Shop All
          </router-link>
          <router-link
            to="/about"
            class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-[#d4c5b0] cursor-pointer hover:text-[#c8a96a] transition-colors block"
          >
            About Us
          </router-link>
          <router-link
            to="/contact"
            class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-[#d4c5b0] cursor-pointer hover:text-[#c8a96a] transition-colors block"
          >
            Contact
          </router-link>
        </div>
      </div>

      <!-- Customer Service -->
      <div class="content-stretch flex flex-col gap-[16px] items-start relative shrink-0">
        <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[24px] not-italic text-[16px] text-[#c8a96a]">Customer Service</p>
        <div class="space-y-2">
          <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-[#d4c5b0]">Shipping & Returns</p>
          <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-[#d4c5b0]">FAQ</p>
          <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-[#d4c5b0]">Privacy Policy</p>
        </div>
      </div>

      <!-- Social Media -->
      <div class="content-stretch flex flex-col gap-[16px] items-start relative shrink-0">
        <p class="font-['Inter:Medium',_sans-serif] font-medium leading-[24px] not-italic text-[16px] text-[#c8a96a]">Connect</p>
        <div class="flex gap-4">
          <!-- Instagram -->
          <a href="#" class="cursor-pointer hover:opacity-80 transition-opacity" aria-label="Instagram">
            <svg class="size-5 text-[#c8a96a]" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zM5.838 12a6.162 6.162 0 1 1 12.324 0 6.162 6.162 0 0 1-12.324 0zM12 16a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm4.965-10.322a1.44 1.44 0 1 1 2.881.001 1.44 1.44 0 0 1-2.881-.001z"/>
            </svg>
          </a>
          <!-- Facebook -->
          <a href="#" class="cursor-pointer hover:opacity-80 transition-opacity" aria-label="Facebook">
            <svg class="size-5 text-[#c8a96a]" fill="currentColor" viewBox="0 0 24 24">
              <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
            </svg>
          </a>
          <!-- Twitter -->
          <a href="#" class="cursor-pointer hover:opacity-80 transition-opacity" aria-label="Twitter">
            <svg class="size-5 text-[#c8a96a]" fill="currentColor" viewBox="0 0 24 24">
              <path d="M23.953 4.57a10 10 0 002.856-3.586c-1.04.464-2.142.881-3.287 1.184a4.92 4.92 0 00-8.869 4.49 13.978 13.978 0 01-10.15-5.144c-.404.69-.621 1.49-.621 2.345 0 1.708.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827c-.396.108-.81.155-1.236.155-.3 0-.593-.028-.88-.082a4.925 4.925 0 004.6 3.417a9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
            </svg>
          </a>
          <!-- Email -->
          <a href="mailto:info@velixier.com" class="cursor-pointer hover:opacity-80 transition-opacity" aria-label="Email">
            <svg class="size-5 text-[#c8a96a]" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
            </svg>
          </a>
        </div>
      </div>
    </div>

    <!-- Copyright -->
    <div class="box-border content-stretch flex flex-col items-start pb-0 pt-[32.667px] px-0 relative w-full border-t border-[rgba(200,169,106,0.2)]">
      <p class="font-['Inter:Regular',_sans-serif] font-normal leading-[20px] not-italic text-[14px] text-center text-[#d4c5b0] w-full">
        © 2025 VELIXIER. All rights reserved.
      </p>
    </div>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()
</script>