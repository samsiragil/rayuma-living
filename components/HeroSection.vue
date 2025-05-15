<template>
  <header
    class="absolute top-6 left-1/2 transform -translate-x-1/2 w-full z-50 px-6">
    <div class="max-w-screen-xl mx-auto">
      <nav
        class="flex justify-between items-center py-4 border-b border-white/10">
        <!-- Logo + Brand Name -->
        <div class="flex items-center gap-3">
          <img
            src="/images/logo2.png"
            alt="Rayuma Living Logo"
            class="w-10 h-10 object-contain" />
          <div class="text-3xl tracking-tight font-serif font-bold text-[#f5f5f5]">
            Rayuma Living
          </div>
        </div>

        <!-- Nav Links -->
        <ul class="flex gap-10 text-sm font-light text-[#f5f5f5]">
          <li>
            <a
              href="#"
              class="transition-colors duration-300 hover:text-[#D4AF37]">
              Home
            </a>
          </li>
          <li>
            <a
              href="#"
              class="transition-colors duration-300 hover:text-[#D4AF37]">
              Properties
            </a>
          </li>
          <li>
            <a
              href="#"
              class="transition-colors duration-300 hover:text-[#D4AF37]">
              Our Projects
            </a>
          </li>
          <li>
            <a
              href="#"
              class="transition-colors duration-300 hover:text-[#D4AF37]">
              Market
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>

  <section
    ref="sectionRef"
    class="relative h-[100vh] flex items-center bg-[#0B0D17] overflow-hidden">
    <div
      class="absolute inset-0 bg-fixed bg-center bg-cover scale-105 opacity-80 transition-all duration-1000"
      :style="{ backgroundImage: 'url(/images/banner.jpg)' }" />

    <div
      class="absolute inset-0 bg-gradient-to-r from-[#0B0D17]/60 to-[#0B0D17]/40 z-0" />

    <div
      class="relative z-10 max-w-screen-xl mx-auto w-full translate-y-9 transition-all duration-1000"
      >
      <h1
        class="text-4xl md:text-8xl font-serif font-semibold text-[#f5f5f5] tracking-tight leading-loose mb-6 text-balance" data-aos="fade-up">
        Invest in Timeless
        <br />
        Tranquility
      </h1>

      <p class="mb-8 text-base lg:text-lg text-[#f5f1e6]/90 max-w-xl" data-aos="fade-up">
        Curated properties in Bali for investors seeking peace, profit, and permanence.
      </p>

      <div class="flex gap-12" data-aos="fade-up">
        <button class="group flex flex-col items-star">
          <div
            class="flex items-center gap-4 text-md text-[#f5f5f5] group-hover:text-[#bfa76f] transition-colors duration-300">
            <span>Explore Properties</span>
            <ArrowUpRight
              class="w-4 h-4 transition-transform group-hover:translate-x-1 group-hover:-translate-y-1" />
          </div>
          <span
            class="mt-3 h-[1px] w-full bg-[#f5f5f5] transition-all group-hover:bg-[#bfa76f]" />
        </button>
        <button class="group flex flex-col items-start text-[#f5f5f5]">
          <div
            class="flex items-center gap-4 text-md text-[#f5f5f5] group-hover:text-[#bfa76f] transition-colors duration-300">
            <span>Schedule a Visit</span>
            <ArrowUpRight
              class="w-4 h-4 transition-transform group-hover:translate-x-1 group-hover:-translate-y-1" />
          </div>
          <span
            class="mt-3 h-[1px] w-full bg-[#f5f5f5] transition-all group-hover:bg-[#bfa76f]" />
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ArrowUpRight } from 'lucide-vue-next';
</script>
