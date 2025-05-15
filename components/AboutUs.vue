<template>
  <section class="bg-[#FAF8F3] py-32 px-4">
    <div class="max-w-screen-xl mx-auto grid md:grid-cols-2 gap-20 items-center">
      <!-- Image Area (rebalanced proportion) -->
      <div class="relative rounded-xl overflow-hidden shadow-xl border border-[#D4C29A] min-h-[540px]" data-aos="zoom-in" data-aos-duration="1300">
        <img
          src="/images/property-3.jpg"
          alt="Elegant tropical living room"
          class="absolute inset-0 w-full h-full object-cover"
        />
      </div>

      <!-- Content Area (center-aligned vertically) -->
      <div class="flex flex-col justify-center h-full">
        <!-- Top line -->
        <div class="w-16 h-1 bg-[#D4C29A] mb-6" data-aos="fade-up" data-aos-delay="0"></div>

        <h2 class="text-4xl font-serif text-[#5E4B3C] font-bold tracking-wide leading-snug mb-4" data-aos="fade-up" data-aos-delay="100">
          An Exclusive Sanctuary in the Heart of Tropical Living
        </h2>
        <p class="text-[#1E1E1E] text-base leading-relaxed tracking-wide mb-10 max-w-md" data-aos="fade-up" data-aos-delay="300">
          Invest in a space where elegance meets tropical soul. Designed to deliver long-term value for refined hospitality.
        </p>

        <!-- Refined Value Points -->
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
          <div
            v-for="(item, index) in values"
            :key="index"
            class="group bg-[#F5F3ED] rounded-md px-5 py-4 transition shadow-sm hover:shadow-md hover:-translate-y-[2px] relative"
            data-aos="fade-up" data-aos-delay="350"
          >
            <!-- Pattern / line embellishment -->
            <div class="absolute left-0 top-4 bottom-4 w-[2px] bg-[#D4C29A]/40 rounded-full group-hover:bg-[#D4C29A] transition"></div>

            <div class="flex items-center gap-3 mb-1 pl-2">
              <div class="w-8 h-8 rounded-full border bg-[#EAE8E2] flex items-center justify-center group-hover:scale-105 transition-transform">
                <component :is="item.icon" class="text-[#5E4B3C] w-4 h-4" />
              </div>
              <h4 class="text-[#5E4B3C] font-semibold text-base">
                {{ item.title }}
              </h4>
            </div>
            <p class="text-sm text-[#8A8D63] leading-snug pl-2">
              {{ item.desc }}
            </p>
          </div>
        </div>

        <!-- CTA -->
        <!-- <button class="bg-[#5E4B3C] text-white text-sm font-medium flex items-center justify-between gap-3 pr-3 pl-5 py-3 rounded-full hover:bg-[#4A3C30] transition group w-fit">
          Book Your Visit
          <span class="bg-white text-[#5E4B3C] w-7 h-7 flex items-center justify-center rounded-full transition-transform group-hover:translate-x-1">
            <ArrowRight class="w-4 h-4" />
          </span>
        </button> -->
      </div>
    </div>
  </section>
</template>

<script setup>
import { Leaf, Layout, RefreshCcw, Home, ArrowRight } from 'lucide-vue-next'

const values = [
  {
    icon: Leaf,
    title: 'Natural Finishing',
    desc: 'Materials that echo nature’s rhythm.',
  },
  {
    icon: Layout,
    title: 'Adaptive Floorplan',
    desc: 'Built to flex with lifestyle or guests.',
  },
  {
    icon: RefreshCcw,
    title: 'Long-Term Value',
    desc: 'Graceful aging, lasting market relevance.',
  },
  {
    icon: Home,
    title: 'Quiet & Private Living',
    desc: 'A serene oasis for premium retreats.',
  },
]
</script>
