<template>
  <section class="py-24 bg-stone-50">
    <div class="max-w-7xl mx-auto px-6">
      <div class="flex justify-between items-end mb-12">
        <div>
          <h2 class="text-3xl font-serif text-stone-900">Latest Works</h2>
          <p class="text-stone-500 mt-2">A glimpse into our signature spaces.</p>
        </div>
        <button class="text-xs font-bold uppercase tracking-widest text-amber-600 border-b-2 border-amber-600 pb-1">View All Projects</button>
      </div>

      <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
        <div v-for="(img, idx) in gallery" :key="idx" class="relative group overflow-hidden rounded-lg">
          <img :src="img" class="w-full h-auto object-cover hover:brightness-50 transition-all duration-500" />
          <div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity">
            <span class="text-white font-serif italic text-lg">View Project</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const gallery = [
  "https://images.unsplash.com/photo-1616489953149-7597b5aa27ee?auto=format&fit=crop&q=80",
  "https://images.unsplash.com/photo-1594026112284-02bb6f3352fe?auto=format&fit=crop&q=80",
  "https://images.unsplash.com/photo-1615873968403-89e068628265?auto=format&fit=crop&q=80",
  "https://images.unsplash.com/photo-1616137422495-1e902b7ca772?auto=format&fit=crop&q=80",
  "https://images.unsplash.com/photo-1616489140336-934c2ba6bc91?auto=format&fit=crop&q=80",
  "https://images.unsplash.com/photo-1560448204-61dc36dc98b8?auto=format&fit=crop&q=80"
]
</script>