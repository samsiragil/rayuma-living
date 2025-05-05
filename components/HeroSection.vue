<template>
  <header class="absolute top-6 left-1/2 transform -translate-x-1/2 w-full z-50 px-6">
    <div class="max-w-screen-xl mx-auto">
      <nav class="flex justify-between items-center py-4 border-b border-white/10">
        <!-- Logo + Brand Name -->
        <div class="flex items-center gap-3">
          <img src="/images/logo-transparent.png" alt="Rayuma Living Logo" class="w-8 h-8 object-contain" />
          <div class="text-lg tracking-wide font-serif text-[#f5f5f5]">
            Rayuma Living
          </div>
        </div>

        <!-- Nav Links -->
        <ul class="flex gap-10 text-sm font-light text-[#f5f5f5]">
          <li><a href="#" class="transition-colors duration-300 hover:text-[#D4AF37]">Home</a></li>
          <li><a href="#" class="transition-colors duration-300 hover:text-[#D4AF37]">Properties</a></li>
          <li><a href="#" class="transition-colors duration-300 hover:text-[#D4AF37]">Our Projects</a></li>
          <li><a href="#" class="transition-colors duration-300 hover:text-[#D4AF37]">Market</a></li>
        </ul>

      </nav>
    </div>
  </header>

  
  <section
    ref="sectionRef"
    class="relative h-[100vh] flex items-center bg-[#0B0D17] overflow-hidden"
  >
    <!-- Background -->
    <div
      class="absolute inset-0 bg-fixed bg-center bg-cover scale-105 blur-sm opacity-80 transition-all duration-1000"
      :style="{ backgroundImage: 'url(/images/hero.jpg)' }"
    />

    <!-- Overlay -->
    <div class="absolute inset-0 bg-gradient-to-r from-[#0B0D17]/70 to-[#0B0D17]/40 z-0" />

    <!-- Content -->
    <div
      class="relative z-10 max-w-screen-xl mx-auto px-6 md:px-12 opacity-0 translate-y-10 transition-all duration-1000 text-center" data-aos="fade-up"
    >
      <h1 class="text-4xl md:text-6xl font-serif font-semibold text-[#f5f5f5] tracking-wide leading-loose mb-9 text-balance">
        Discover Timeless Elegance with <br /><span class="text-[#D4AF37]">Rayuma Living</span>
      </h1>

      <p class="text-lg md:text-xl text-gray-300 font-sans max-w-xl mx-auto leading-relaxed mb-9">
        Explore a world of luxurious properties that reflect prestige, comfort, and architectural brilliance.
      </p>

      <NuxtLink
        to="#properties"
        class="group bg-[#D4AF37] hover:bg-yellow-500 text-black font-semibold px-6 py-3 rounded-full shadow-lg transition inline-flex items-center gap-2"
      >
        View Listings
        <MoveRight
          class="text-black transform transition-transform duration-300 group-hover:translate-x-1.5"
        />
      </NuxtLink>


    </div>
  </section>
</template>

<script setup>
import { MoveRight } from 'lucide-vue-next';
</script>
