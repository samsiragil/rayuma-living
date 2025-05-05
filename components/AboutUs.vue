
<template>
  <section class="bg-[#f9f9f9] py-20">
    <div class="container mx-auto px-4 flex flex-col-reverse lg:flex-row items-center gap-12">
      <!-- Text Content -->
      <div class="lg:w-1/2">
        <h2 class="text-3xl lg:text-4xl font-semibold leading-snug text-[#bfa76f] font-serif mb-4">
          Our Story Begins in Bali
        </h2>
        <p class="text-zinc-700 text-base lg:text-lg mb-4 font-sans">
          Rayuma Living was founded with a single belief: that real estate should be about soul, vision, and legacy — not just buildings.
        </p>
        <p class="text-zinc-700 text-base lg:text-lg font-sans">
          Our roots are in Bali, but our mindset is global. We combine timeless design, architectural harmony, and bespoke client service to craft properties that define prestige and permanence.
        </p>
        <p class="italic text-sm text-zinc-500 mt-6">"Rooted in Bali. Inspired by the world."</p>
      </div>

      <!-- Image with overlay -->
      <div class="lg:w-1/2 relative rounded-xl shadow-lg overflow-hidden">
        <img
          src="/images/property-10.jpg"
          alt="Rayuma Team Office"
          class="object-cover w-full h-full rounded-xl"
        />
        <div class="absolute bottom-4 left-4 bg-white/80 px-4 py-2 rounded shadow text-center">
          <p class="text-xs uppercase font-semibold tracking-wider text-zinc-500">Established</p>
          <p class="text-xl font-serif text-[#bfa76f]">2018</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional logic needed
</script>
