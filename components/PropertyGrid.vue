<template>
  <section class="py-16 bg-white">
    <div class="max-w-screen-xl mx-auto px-4">
      <div class="text-center mb-10" data-aos="fade-up">
        <h2 class="text-3xl lg:text-4xl font-serif font-semibold text-[#D4AF37] leading-snug">Our Exclusive Listings</h2>
        <p class="text-base lg:text-lg text-[#3f3f3f] mt-2">
          Discover handpicked properties from Bali's most prestigious locations.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="(property, index) in properties"
          :key="index"
          class="relative rounded-3xl overflow-hidden shadow-xl group"
          data-aos="zoom-in"
        >
          <div class="overflow-hidden relative h-[420px]">
            <img
              :src="`/images/${property.image}`"
              :alt="property.title"
              class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700 ease-out"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/30 to-transparent transition duration-700 ease-out group-hover:from-black/90" />
            <div class="absolute bottom-0 w-full p-6 z-10 flex flex-col gap-3">
              <h3 class="text-white text-lg lg:text-xl font-serif font-medium tracking-wide leading-snug">
                {{ property.name }}
              </h3>
              <p class="text-white/80 text-sm leading-tight">
                Location: {{ property.location }}
              </p>
              <p class="text-[#D4AF37] text-lg lg:text-xl font-semibold tracking-wide">
                {{ property.price }}
              </p>
              <button
                class="mt-1 px-6 py-3 bg-white/10 text-white border border-[#D4AF37] rounded-full tracking-wide 
                hover:bg-[#D4AF37] hover:text-black hover:shadow-xl transition-all duration-500 ease-in-out backdrop-blur-sm"
              >
                View Details
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { MoveRight } from 'lucide-vue-next'

const properties = [
  {
    name: 'Luxury Modern Villa',
    location: 'Sunset Bay, Bali',
    price: '$350,000',
    image: 'property-1.jpg',
  },
  {
    name: 'The Uluwatu Residence',
    location: 'Uluwatu, Bali',
    price: '$720,000',
    image: 'property-2.jpg',
  },
  {
    name: 'Seminyak Garden Loft',
    location: 'Seminyak, Bali',
    price: '$490,000',
    image: 'property-3.jpg',
  },
  {
    name: 'Canggu Beachfront Estate',
    location: 'Canggu, Bali',
    price: '$1,100,000',
    image: 'property-4.jpg',
  },
]
</script>

<style scoped>
/* Optional: smooth hover effect on card */
.group:hover img {
  transform: scale(1.02);
  transition: transform 0.5s ease;
}
</style>
