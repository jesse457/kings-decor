<template>
  <section class="relative h-screen w-full overflow-hidden">
    <!-- Background: Dark luxury aesthetic -->
    <div class="absolute inset-0 bg-stone-900">
      <img 
        src="https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=2070&auto=format&fit=crop" 
        class="w-full h-full object-cover opacity-60 animate-slow-zoom"
        alt="Kings Decor Wedding Setup"
      />
      <div class="absolute inset-0 bg-gradient-to-t from-stone-900 via-stone-900/20 to-transparent"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 h-full flex flex-col justify-center px-6 md:px-20 max-w-8xl mx-auto">
      <div class="max-w-4xl space-y-6">
        <div class="flex items-center gap-4">
          <span class="h-[1px] w-12 bg-amber-200"></span>
          <p class="text-amber-200 uppercase tracking-[0.3em] text-xs font-semibold">Cameroon's Finest</p>
        </div>
        
        <h1 class="text-6xl md:text-9xl font-serif text-white leading-[0.9] tracking-tight">
          We Set The <br />
          <span class="italic text-white/90">Atmosphere.</span>
        </h1>
        
        <p class="text-stone-300 text-lg md:text-xl font-light max-w-xl leading-relaxed mt-4">
          From the intimacy of a Bed Day to the grandeur of a Royal Wedding. We don't just decorate spaces; we curate memories.
        </p>

        <div class="pt-8 flex gap-4">
          <button class="bg-white text-stone-900 px-8 py-4 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-amber-200 transition-colors duration-300">
            Book an Event
          </button>
          <button class="px-8 py-4 rounded-full text-white border border-white/30 font-bold uppercase tracking-widest text-xs hover:bg-white/10 backdrop-blur-md transition-all">
            View Gallery
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.animate-slow-zoom {
  animation: zoomEffect 20s infinite alternate;
}
@keyframes zoomEffect {
  from { transform: scale(1); }
  to { transform: scale(1.1); }
}
</style>