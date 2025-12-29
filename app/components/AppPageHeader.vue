<template>
  <div class="relative h-[50vh] flex items-center justify-center overflow-hidden bg-stone-950">
    <!-- Background Image -->
    <div class="absolute inset-0">
      <img :src="image" alt="" aria-hidden="true" class="w-full h-full object-cover opacity-60" />
      <div class="absolute inset-0 bg-black/50"></div>
    </div>
    
    <!-- Title -->
    <div class="relative z-10 text-center px-4 max-w-4xl mx-auto">
      <p v-if="subtitle" class="text-accent text-xs md:text-sm font-bold uppercase tracking-[0.3em] mb-6 animate-fade-in-up">
        {{ subtitle }}
      </p>
      <h1 class="text-5xl md:text-7xl lg:text-8xl font-serif text-white animate-fade-in-up delay-100 drop-shadow-lg">
        {{ title }}
      </h1>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  subtitle: String,
  image: String
})
</script>

<style scoped>
.delay-100 { animation-delay: 100ms; }
</style>