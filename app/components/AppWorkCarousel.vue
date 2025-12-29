<template>
  <section class="bg-stone-900 py-32 overflow-hidden">
    <div class="px-6 md:px-12 max-w-7xl mx-auto mb-12 flex justify-between items-end">
      <div>
        <h2 class="text-4xl md:text-5xl font-serif text-white">Recent Masterpieces</h2>
        <p class="text-stone-400 mt-2">Swipe to explore our latest installations.</p>
      </div>
      
      <!-- Navigation Buttons -->
      <div class="flex gap-2">
        <button @click="scroll('left')" class="w-12 h-12 rounded-full border border-stone-700 text-white flex items-center justify-center hover:bg-white hover:text-stone-900 transition">←</button>
        <button @click="scroll('right')" class="w-12 h-12 rounded-full border border-stone-700 text-white flex items-center justify-center hover:bg-white hover:text-stone-900 transition">→</button>
      </div>
    </div>

    <!-- Scroll Container -->
    <div 
      ref="scrollContainer" 
      class="flex gap-6 overflow-x-auto px-6 md:px-12 pb-10 snap-x snap-mandatory scrollbar-hide"
    >
      <div 
        v-for="(work, index) in works" 
        :key="index"
        class="min-w-[85vw] md:min-w-[400px] h-[500px] relative snap-center group rounded-xl overflow-hidden bg-stone-800"
      >
        <img :src="work.img" class="w-full h-full object-cover opacity-80 group-hover:opacity-100 transition duration-500" />
        
        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent"></div>
        
        <div class="absolute bottom-0 left-0 p-6">
          <div class="text-amber-400 text-xs font-bold tracking-widest uppercase mb-1">{{ work.category }}</div>
          <h3 class="text-2xl font-serif text-white">{{ work.title }}</h3>
          <p class="text-stone-400 text-sm mt-1">{{ work.location }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const scrollContainer = ref(null)

const scroll = (direction) => {
  if (scrollContainer.value) {
    const scrollAmount = direction === 'left' ? -400 : 400
    scrollContainer.value.scrollBy({ left: scrollAmount, behavior: 'smooth' })
  }
}

const works = [
  { title: "The Ngu Wedding", location: "Douala, Bonanjo", category: "Wedding", img: "https://images.unsplash.com/photo-1511795409834-ef04bbd61622?auto=format&fit=crop&q=80" },
  { title: "Mami Sarah's Celebration", location: "Yaoundé, Bastos", category: "Funeral Service", img: "https://images.unsplash.com/photo-1478146896981-b80c463643f8?auto=format&fit=crop&q=80" },
  { title: "Private Villa Bed Day", location: "Kribi", category: "Bed Day", img: "https://images.unsplash.com/photo-1616047006789-b7af5afb8c2e?auto=format&fit=crop&q=80" },
  { title: "Golden Jubilee", location: "Limbe", category: "Event", img: "https://images.unsplash.com/photo-1469334031218-e382a71b716b?auto=format&fit=crop&q=80" },
]
</script>

<style scoped>
/* Hide scrollbar for clean look */
.scrollbar-hide::-webkit-scrollbar {
    display: none;
}
.scrollbar-hide {
    -ms-overflow-style: none;
    scrollbar-width: none;
}
</style>