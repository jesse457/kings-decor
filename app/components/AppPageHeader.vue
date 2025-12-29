<template>
  <div class="relative h-[50vh] flex items-center justify-center overflow-hidden bg-stone-900">
    <!-- Background Image -->
    <div class="absolute inset-0">
      <img :src="image" class="w-full h-full object-cover opacity-50" />
      <div class="absolute inset-0 bg-stone-900/40"></div>
    </div>
    
    <!-- Title -->
    <div class="relative z-10 text-center px-4">
      <p v-if="subtitle" class="text-amber-400 text-xs font-bold uppercase tracking-[0.3em] mb-4 animate-fade-in-up">
        {{ subtitle }}
      </p>
      <h1 class="text-5xl md:text-7xl font-serif text-white animate-fade-in-up delay-100">
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