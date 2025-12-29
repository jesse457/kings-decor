<template>
  <div>
    <!-- 1. The Cinematic Hero -->
    <AppHero />

    <!-- 2. Occasions (Bed Days, Funerals, Weddings) -->
    <AppOccasions />

    <!-- 3. The Work Carousel (Scroll Snap) -->
    <AppWorkCarousel />

    <!-- 4. Final Home CTA -->
    <section class="py-24 bg-stone-900 text-white relative overflow-hidden">
      <!-- Decorative background glow -->
      <div class="absolute top-0 right-0 w-96 h-96 bg-amber-600/20 blur-[100px] rounded-full"></div>

      <div class="relative z-10 max-w-4xl mx-auto px-6 text-center">
        <h2 class="text-4xl md:text-6xl font-serif mb-6">Ready to Transform Your Space?</h2>
        <p class="text-stone-400 text-lg mb-10 font-light">
          Whether it's a private Bed Day in Douala or a Grand Wedding in Yaoundé, 
          let's discuss how we can bring the "Kings" touch to your event.
        </p>
        <div class="flex flex-col sm:flex-row justify-center gap-4">
          <NuxtLink to="/contact">
            <button class="w-full sm:w-auto bg-amber-600 text-white px-10 py-4 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-white hover:text-stone-900 transition-colors duration-300">
              Get A Free Quote
            </button>
          </NuxtLink>
          <NuxtLink to="/portfolio">
            <button class="w-full sm:w-auto border border-stone-700 text-white px-10 py-4 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-stone-800 transition-colors">
              See More Work
            </button>
          </NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>