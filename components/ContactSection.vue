<template>
  <section class="py-20 px-6 bg-white" id="contact">
    <div class="max-w-4xl mx-auto text-center mb-12">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-800">Get in Touch</h2>
      <p class="mt-2 text-gray-600">
        Interested in a property or need consultation? We’re here to help you make the right move.
      </p>
    </div>

    <form class="max-w-2xl mx-auto grid gap-6 text-left">
      <div class="grid md:grid-cols-2 gap-6">
        <input type="text" placeholder="Your Name" class="input" />
        <input type="email" placeholder="Email Address" class="input" />
      </div>
      <textarea rows="5" placeholder="Your Message" class="input" />
      <button
        type="submit"
        class="bg-emerald-500 hover:bg-emerald-600 text-white py-3 px-6 rounded-xl font-semibold transition w-fit"
      >
        Send Message
      </button>
    </form>
  </section>
</template>

<style scoped>
.input {
  @apply w-full border border-gray-300 rounded-lg p-3 text-gray-700 focus:outline-none focus:ring-2 focus:ring-emerald-400;
}
</style>
