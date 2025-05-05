<template>
  <section class="pt-24 pb-28 bg-white">
    <div class="max-w-6xl mx-auto px-6 flex flex-col lg:flex-row items-center gap-12">
      <!-- Image -->
      <div class="w-full lg:w-1/2">
        <img
          src="/images/property-10.jpg"
          alt="Luxury Experience"
          class="rounded-2xl shadow-xl object-cover w-full h-full max-h-[500px]"
        />
      </div>

      <!-- Text Content -->
      <div class="w-full lg:w-1/2 space-y-6">
        <h2 class="text-3xl lg:text-4xl font-serif font-semibold text-[#bfa76f] leading-snug">
          Why Choose Rayuma Living?
        </h2>
        <p class="text-base lg:text-lg text-[#3f3f3f] mt-2">
          We provide a seamless and luxurious property experience in Bali, tailored to your lifestyle
          and investment goals.
        </p>
        <ul class="space-y-4">
          <li class="flex items-start gap-4">
            <ShieldCheck class="text-[#B19857] w-6 h-6 mt-1" />
            <span class="text-base text-gray-700">
              Trusted by over 500+ high-net-worth clients
            </span>
          </li>
          <li class="flex items-start gap-4">
            <Gem class="text-[#B19857] w-6 h-6 mt-1" />
            <span class="text-base text-gray-700">
              Curated collection of exclusive luxury properties
            </span>
          </li>
          <li class="flex items-start gap-4">
            <PhoneCall class="text-[#B19857] w-6 h-6 mt-1" />
            <span class="text-base text-gray-700">
              Dedicated concierge team and personalized service
            </span>
          </li>
          <li class="flex items-start gap-4">
            <Stars class="text-[#B19857] w-6 h-6 mt-1" />
            <span class="text-base text-gray-700">
              Exceptional market knowledge and legal support
            </span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ShieldCheck, Stars, Gem, PhoneCall } from 'lucide-vue-next'
</script>
