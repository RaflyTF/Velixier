<script setup lang="ts">
const testimonials = [
  {
    name: 'Zann',
    role: 'Yapper',
    review:
      'Beautifully packaged, authentic fragrance, and such a pleasant aroma that lasts all day. Shopping here was an amazing experience!',
  },
  {
    name: 'Black Daniel',
    role: 'Vtuber',
    review:
      'The perfume arrived quickly and was exactly as described — the scent is elegant and long-lasting, truly exceeded my expectations',
  },
]
</script>

<template>
  <div class="relative px-[120px] py-20 bg-[#0d0c0a]">
    <div class="flex flex-col gap-[50px] items-center w-full max-w-[1400px] mx-auto">
      <div
        class="flex flex-col font-['Playfair_Display'] font-bold justify-center text-[36px] text-[#c8a96a] text-center w-full"
      >
        <p>What our customer says</p>
      </div>
      <div class="flex items-start justify-center w-full gap-12 flex-wrap">
        <div
          v-for="(testimonial, idx) in testimonials"
          :key="idx"
          class="bg-[#1a1613] h-[320px] overflow-clip relative rounded-[24px] shadow-[0px_8px_24px_rgba(0,0,0,0.4)] flex-1 min-w-[300px] max-w-[580px] border border-[rgba(200,169,106,0.2)] hover:border-[rgba(200,169,106,0.4)] transition-all duration-300"
        >
          <div class="flex flex-col gap-[24px] items-start px-[32px] pt-[32px] pb-[32px]">
            <div class="flex justify-between items-center w-full">
              <div class="flex gap-[16px] items-center">
                <div
                  class="h-[80px] w-[80px] bg-[#c8a96a] rounded-full flex items-center justify-center shrink-0"
                >
                  <p class="font-['Playfair_Display'] font-bold text-[28px] text-[#1a1613]">
                    {{ testimonial.name.charAt(0) }}
                  </p>
                </div>
                <div class="flex flex-col gap-[4px] items-start">
                  <p class="font-['Playfair_Display'] font-bold text-[20px] text-[#c8a96a]">
                    {{ testimonial.name }}
                  </p>
                  <p class="font-['Inter'] text-[14px] text-[#d4c5b0]">{{ testimonial.role }}</p>
                </div>
              </div>
              <div class="flex gap-1 shrink-0">
                <svg v-for="i in 5" :key="i" class="size-[18px]" fill="#c8a96a" viewBox="0 0 24 24">
                  <path
                    d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                  />
                </svg>
              </div>
            </div>
            <p class="font-['Inter'] text-[15px] leading-[1.7] text-[#d4c5b0]">
              {{ testimonial.review }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
