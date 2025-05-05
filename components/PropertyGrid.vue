<template>
  <section id="properties" class="pt-24 pb-28 px-4 bg-zinc-50">
    <div class="max-w-screen-xl mx-auto">
      <div class="text-center mb-10">
        <h2 class="text-3xl lg:text-4xl font-serif font-semibold text-[#D4AF37] leading-snug">Our Exclusive Listings</h2>
        <p class="text-base lg:text-lg text-[#3f3f3f] mt-2">
          Discover handpicked properties from Bali's most prestigious locations.
        </p>
      </div>

      <div class="relative">
        <div
          ref="slider"
          class="keen-slider overflow-visible"
        >
          <div
            v-for="(property, index) in properties"
            :key="index"
            class="keen-slider__slide px-4 relative rounded-xl overflow-hidden shadow-md group"
          >
            <img
              :src="`/images/property-${index + 1}.jpg`"
              :alt="property.title"
              class="w-full h-72 object-cover transition-transform duration-500 group-hover:scale-105"
            />
            <div
              class="absolute inset-0 bg-black/50 flex flex-col justify-end p-5"
            >
              <div class="text-white mb-4">
                <h3 class="text-lg font-semibold leading-tight">{{ property.title }}</h3>
                <p class="text-sm opacity-90">Location : {{ property.location }}</p>
                <p class="text-sm opacity-90">Price : {{ property.price }}</p>
              </div>
              <button
                class="w-full bg-[#bfa76f]/90 hover:bg-[#bfa76f] text-white text-sm font-medium py-2 rounded-full transition-colors"
              >
                Details
              </button>
            </div>
          </div>
        </div>

        <!-- Navigation -->
        <button
          @click="prevSlide"
          class="absolute left-0 top-1/2 -translate-y-1/2 z-10 w-10 h-10 rounded-full border border-[#bfa76f] text-[#bfa76f] bg-white hover:bg-[#bfa76f] hover:text-white transition shadow"
        >
          <ChevronLeft class="w-5 h-5 mx-auto" />
        </button>
        <button
          @click="nextSlide"
          class="absolute right-0 top-1/2 -translate-y-1/2 z-10 w-10 h-10 rounded-full border border-[#bfa76f] text-[#bfa76f] bg-white hover:bg-[#bfa76f] hover:text-white transition shadow"
        >
          <ChevronRight class="w-5 h-5 mx-auto" />
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { ChevronLeft, ChevronRight } from 'lucide-vue-next'
import KeenSlider from 'keen-slider'
import 'keen-slider/keen-slider.min.css'

const slider = ref(null)
let keenInstance = null

const properties = [
  { title: 'Sunset Garden Villa', location: 'Kerobokan, Bali', price: 520000 },
  { title: 'Minimalist River House', location: 'Tabanan, Bali', price: 470000 },
  { title: 'Royal Hill Residence', location: 'Jimbaran Hills, Bali', price: 750000 },
  { title: 'Ocean Breeze Penthouse', location: 'Pantai Berawa, Canggu', price: 690000 },
  { title: 'Tropical Jungle Hideaway', location: 'Jalan Sweta, Ubud', price: 410000 },
  { title: 'Seminyak Luxe Estate', location: 'Jalan Kayu Aya, Seminyak', price: 980000 },
  { title: 'Clifftop Infinity Villa', location: 'Jalan Goa Gong, Jimbaran', price: 820000 },
  { title: 'Balangan Oceanview Home', location: 'Balangan Beach, Bali', price: 615000 },
  { title: 'Ubud Bamboo Residence', location: 'Tegallalang, Ubud', price: 390000 },
  { title: 'Alila Clifftop Retreat', location: 'Pecatu, Bali', price: 1120000 },
]

onMounted(() => {
  keenInstance = new KeenSlider(slider.value, {
    loop: false,
    slides: {
      perView: 4,
      spacing: 32,
    },
    breakpoints: {
      '(max-width: 1024px)': {
        slides: { perView: 1.2, spacing: 16 },
      },
      '(max-width: 640px)': {
        slides: { perView: 1.1, spacing: 12 },
      },
    },
  })
})

const nextSlide = () => {
  keenInstance?.next()
}
const prevSlide = () => {
  keenInstance?.prev()
}
</script>

<style scoped>
.keen-slider__slide {
  flex-shrink: 0;
}
</style>
