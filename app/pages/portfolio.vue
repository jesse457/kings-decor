<template>
  <div>
    <AppPageHeader 
      title="Our Masterpieces" 
      subtitle="Gallery"
      image="https://images.unsplash.com/photo-1519225421980-715cb0202128?auto=format&fit=crop&q=80"
    />

    <section class="py-20 px-6 max-w-7xl mx-auto">
      <!-- Filters -->
      <div class="flex flex-wrap justify-center gap-6 mb-16" role="tablist" aria-label="Portfolio Category Filter">
        <button 
          v-for="cat in categories" 
          :key="cat"
          @click="activeCategory = cat"
          class="text-xs uppercase tracking-widest px-4 py-2 border rounded-full transition-all duration-300 font-sans"
          :class="activeCategory === cat ? 'bg-primary text-primary-foreground border-primary' : 'text-muted-foreground border-border hover:border-primary hover:text-primary'"
          :aria-selected="activeCategory === cat"
          role="tab"
        >
          {{ cat }}
        </button>
      </div>

      <!-- Masonry Grid -->
      <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
        <div 
          v-for="(item, index) in filteredItems" 
          :key="index"
          class="break-inside-avoid relative group overflow-hidden rounded-lg cursor-zoom-in"
        >
          <img 
            :src="item.image" 
            :alt="item.title + ' - ' + item.desc"
            class="w-full h-auto object-cover transition duration-700 group-hover:scale-110" 
          />
          
          <!-- Overlay -->
          <div class="absolute inset-0 bg-primary/80 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-8">
            <span class="text-accent text-xs font-bold uppercase tracking-widest font-sans">{{ item.category }}</span>
            <h3 class="text-white font-serif text-2xl mt-1 italic">{{ item.title }}</h3>
            <p class="text-white/80 text-sm mt-2 font-sans">{{ item.desc }}</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const activeCategory = ref('All')
const categories = ['All', 'Weddings', 'Bed Days', 'Funerals', 'Corporate']

const portfolio = [
  { title: "Nguea Traditional Wedding", category: "Weddings", desc: "Gold & Royal Blue Theme", image: "https://images.unsplash.com/photo-1511795409834-ef04bbd61622?auto=format&fit=crop&q=80" },
  { title: "Little Prince Arrival", category: "Bed Days", desc: "Soft linens and cloud aesthetics", image: "https://images.unsplash.com/photo-1513278974582-dc34a6ed106e?auto=format&fit=crop&q=80" },
  { title: "Pa Njoya Celebration of Life", category: "Funerals", desc: "Dignified white florals", image: "https://images.unsplash.com/photo-1596525727632-6a6873321528?auto=format&fit=crop&q=80" },
  { title: "MTN Corporate Gala", category: "Corporate", desc: "Lighting & Stage Design", image: "https://images.unsplash.com/photo-1505236858219-8359eb29e329?auto=format&fit=crop&q=80" },
  { title: "White Wedding at Hilton", category: "Weddings", desc: "Crystal centerpieces", image: "https://images.unsplash.com/photo-1520342868574-5fa3804e551c?auto=format&fit=crop&q=80" },
  { title: "Intimate Homecoming", category: "Bed Days", desc: "Mother care setup", image: "https://images.unsplash.com/photo-1616489953149-7597b5aa27ee?auto=format&fit=crop&q=80" },
]

const filteredItems = computed(() => {
  if (activeCategory.value === 'All') return portfolio
  return portfolio.filter(item => item.category === activeCategory.value)
})
</script>