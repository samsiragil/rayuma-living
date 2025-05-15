<template>
  <section class="py-32 bg-white relative">
    <div class="max-w-screen-xl mx-auto px-4 md:px-8">
      <!-- Title & Description -->
      <div class="text-center mb-14">
        <!-- Top line -->
        <div class="w-16 h-1 bg-[#D4C29A] mb-6 mx-auto" data-aos="fade-up" data-aos-delay="0"></div>
        <h2 class="text-4xl font-serif text-[#5E4B3C] font-bold tracking-wide leading-snug mb-4" data-aos="fade-up" data-aos-delay="100">
          Welcome to Serenity
        </h2>
        <p class="text-[#1E1E1E] max-w-xl mx-auto mb-0" data-aos="fade-up" data-aos-delay="300">
          From luxurious suites to personalized experiences, Serenity Hotel is
          designed to make every guest feel at home. Discover the perfect blend
          of nature, elegance, and warmth.
        </p>
      </div>

      <!-- Gallery Grid -->
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 grid-flow-row-dense">
        <div
          v-for="(img, index) in images"
          :key="index"
          class="relative rounded-xl shadow-xl border border-[#D4C29A] group transform transition duration-700 overflow-hidden"
          :class="[
            index === 1 || index === 4 ? 'h-[320px]' : 'h-[260px]',
            index === 0 || index === 2 ? 'self-end' : '',
          ]"
          data-aos="zoom-in" data-aos-delay="350"
          @click="openLightbox(img)">

          <img
            :src="`/images/${img}`"
            alt="Visual"
            class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300 rounded-xl"
            loading="lazy" />
        </div>
      </div>

      <!-- Lightbox -->
      <div
        v-if="lightboxImage"
        class="fixed inset-0 bg-black bg-opacity-80 flex items-center justify-center z-50"
        @click.self="closeLightbox">
        <img
          :src="`/images/${lightboxImage}`"
          class="max-h-[90vh] max-w-[90vw] rounded-xl shadow-lg" />
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const images = [
  'property-2.jpg',
  'property-4.jpg',
  'property-3.jpg',
  'property-9.jpg',
  'property-5.jpg',
  'property-10.jpg',
];

const reveal = ref(images.map(() => false));

const lightboxImage = ref(null);
function openLightbox(image) {
  lightboxImage.value = image;
}
function closeLightbox() {
  lightboxImage.value = null;
}
</script>
