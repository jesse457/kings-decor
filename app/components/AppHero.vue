<template>
  <section class="relative h-[100dvh] w-full overflow-hidden">
    <!-- Background -->
    <div class="absolute inset-0 bg-stone-950">
      <img 
        src="https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=2070&auto=format&fit=crop" 
        class="w-full h-full object-cover opacity-60 animate-ken-burns"
        alt="Kings Decor Luxury Wedding Setup"
      />
      <div class="absolute inset-0 bg-gradient-to-b from-black/60 via-transparent to-black/80"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 h-full flex flex-col justify-center px-6 md:px-12 max-w-7xl mx-auto pt-20 mt-15">
      <div class="max-w-4xl space-y-8 animate-fade-up">
        <div class="flex items-center gap-4">
          <span class="h-[1px] w-12 bg-accent"></span>
          <p class="text-accent uppercase tracking-[0.3em] text-xs font-bold font-sans">Cameroon's Premier Event Stylists</p>
        </div>
        
        <h1 class="text-5xl md:text-8xl lg:text-9xl font-serif text-white leading-[0.9] tracking-tight">
          We Curate <br />
          <span class="italic text-stone-300">The Unforgettable.</span>
        </h1>
        
        <p class="text-stone-300 text-lg md:text-xl font-light max-w-xl leading-relaxed border-l-2 border-primary pl-6 font-sans">
          From intimate Bed Days in Douala to Grand Weddings in Yaoundé. We bring the "Kings" touch to your most sacred moments.
        </p>

        <div class="pt-8 flex flex-wrap gap-4">
          <NuxtLink to="/contact">
            <button class="bg-primary text-primary-foreground px-10 py-4 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-accent hover:text-accent-foreground hover:scale-105 transition-all duration-300 shadow-lg shadow-black/20">
              Start Your Journey
            </button>
          </NuxtLink>
          <NuxtLink to="/portfolio">
            <button class="px-10 py-4 rounded-full text-white border border-stone-600 font-bold uppercase tracking-widest text-xs hover:bg-white hover:text-stone-900 transition-all duration-300 backdrop-blur-sm">
              View Gallery
            </button>
          </NuxtLink>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="absolute bottom-10 left-1/2 -translate-x-1/2 text-white animate-bounce flex flex-col items-center gap-2 opacity-70">
      <span class="text-[10px] uppercase tracking-widest">Scroll</span>
      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
    </div>
  </section>
</template>

<style scoped>
.animate-ken-burns {
  animation: kenBurns 25s infinite alternate ease-in-out;
}
.animate-fade-up {
  animation: fadeUp 1s ease-out forwards;
}
@keyframes kenBurns {
  0% { transform: scale(1); }
  100% { transform: scale(1.15); }
}
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>