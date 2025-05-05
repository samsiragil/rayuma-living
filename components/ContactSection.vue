<template>
  <section class="py-24 px-6 bg-white" id="contact">
    <div class="max-w-4xl mx-auto text-center mb-16">
      <h2 class="text-3xl md:text-4xl font-serif font-semibold text-gray-800">
        Get in Touch
      </h2>
      <p class="mt-3 text-gray-600 font-sans text-lg">
        Ready to take the next step? We’d love to hear from you.
      </p>
    </div>

    <form
      class="max-w-2xl mx-auto grid gap-6 text-left bg-gray-50 p-8 rounded-2xl shadow"
    >
      <div class="grid md:grid-cols-2 gap-6">
        <input type="text" placeholder="Your Name" class="input" />
        <input type="email" placeholder="Email Address" class="input" />
      </div>
      <textarea rows="5" placeholder="Your Message" class="input" />
      <button
        type="submit"
        class="bg-emerald-500 hover:bg-emerald-600 text-white py-3 px-6 rounded-full font-semibold transition w-fit"
      >
        Send Message
      </button>
    </form>
  </section>
</template>

<style scoped>
.input {
  @apply w-full border border-gray-300 rounded-lg p-3 text-gray-700 font-sans focus:outline-none focus:ring-2 focus:ring-emerald-400;
}
</style>
