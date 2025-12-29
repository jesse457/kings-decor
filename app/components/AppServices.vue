<template>
  <section class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-6">
      <div class="text-center max-w-2xl mx-auto mb-20">
        <h2 class="text-3xl md:text-5xl font-serif mb-6 text-stone-900">Crafting Elegance</h2>
        <p class="text-stone-500 leading-relaxed">Whether it's a private residence or a corporate headquarters, our services are tailored to reflect prestige and functionality.</p>
      </div>

      <div class="grid md:grid-cols-3 gap-12">
        <div v-for="(service, index) in services" :key="index" class="group">
          <div class="relative overflow-hidden mb-8 aspect-square bg-stone-100">
            <img :src="service.image" :alt="service.title" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-700 group-hover:scale-110" />
            <div class="absolute bottom-0 left-0 p-6">
              <span class="text-4xl font-serif text-white/20">0{{ index + 1 }}</span>
            </div>
          </div>
          <h3 class="text-xl font-serif mb-3 text-stone-900 group-hover:text-amber-600 transition-colors">{{ service.title }}</h3>
          <p class="text-stone-500 text-sm leading-relaxed mb-4">{{ service.description }}</p>
          <div class="w-8 h-1 bg-amber-500/30 group-hover:w-20 transition-all duration-500"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: "Interior Architecture",
    description: "Structural design and spatial planning for villas and modern offices across Cameroon.",
    image: "https://images.unsplash.com/photo-1618219908412-a29a1bb7b86e?auto=format&fit=crop&q=80"
  },
  {
    title: "Bespoke Furnishing",
    description: "Hand-crafted furniture made from premium local Mahogany and imported velvet textures.",
    image: "https://images.unsplash.com/photo-1556228453-efd6c1ff04f6?auto=format&fit=crop&q=80"
  },
  {
    title: "Project Management",
    description: "End-to-end supervision of your decor project to ensure royalty-grade finishing.",
    image: "https://images.unsplash.com/photo-1507652313519-d4e9174996dd?auto=format&fit=crop&q=80"
  }
]
</script>