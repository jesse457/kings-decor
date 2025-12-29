<template>
  <nav 
    class="fixed top-0 w-full z-50 transition-all duration-500 border-b border-transparent"
    :class="[
      isScrolled ? 'bg-white/80 backdrop-blur-xl py-4 shadow-sm border-stone-200/50' : 'bg-transparent py-6'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex items-center justify-between">
      
      <!-- 1. Logo -->
      <NuxtLink to="/" class="flex items-center gap-2 z-50 relative">
        <span class="text-2xl font-serif font-bold tracking-tighter uppercase transition-colors duration-300" 
              :class="(isScrolled || isMobileOpen) ? 'text-stone-900' : 'text-white'">
          Kings<span class="text-amber-500">.</span>
        </span>
      </NuxtLink>

      <!-- 2. Desktop Links -->
      <div class="hidden md:flex gap-10 items-center">
        <NuxtLink 
          v-for="link in links" 
          :key="link.name" 
          :to="link.path"
          class="text-xs font-bold uppercase tracking-[0.2em] transition-colors duration-300 hover:text-amber-500"
          :class="isScrolled ? 'text-stone-600' : 'text-white/90'"
        >
          {{ link.name }}
        </NuxtLink>
      </div>

      <!-- 3. Desktop CTA -->
      <div class="hidden md:block">
        <NuxtLink to="/contact">
          <button class="bg-amber-600 text-white px-7 py-3 rounded-full text-xs font-bold uppercase tracking-widest hover:bg-stone-900 hover:scale-105 transition-all duration-300 shadow-lg shadow-amber-900/20">
            Book Now
          </button>
        </NuxtLink>
      </div>

      <!-- 4. Mobile Hamburger Button -->
      <button @click="isMobileOpen = !isMobileOpen" class="md:hidden z-50 relative group">
        <div class="w-8 h-6 flex flex-col justify-between">
          <span class="h-[2px] w-full bg-current transition-all duration-300" :class="(isScrolled || isMobileOpen) ? 'bg-stone-900' : 'bg-white'" :style="isMobileOpen ? 'transform: rotate(45deg) translate(6px, 6px)' : ''"></span>
          <span class="h-[2px] w-full bg-current transition-all duration-300" :class="(isScrolled || isMobileOpen) ? 'bg-stone-900' : 'bg-white'" :style="isMobileOpen ? 'opacity: 0' : ''"></span>
          <span class="h-[2px] w-full bg-current transition-all duration-300" :class="(isScrolled || isMobileOpen) ? 'bg-stone-900' : 'bg-white'" :style="isMobileOpen ? 'transform: rotate(-45deg) translate(5px, -5px)' : ''"></span>
        </div>
      </button>

      <!-- 5. Mobile Full Screen Menu -->
      <div 
        class="fixed inset-0 bg-white z-40 flex flex-col items-center justify-center gap-8 transition-all duration-500 md:hidden"
        :class="isMobileOpen ? 'translate-x-0 opacity-100' : 'translate-x-full opacity-0'"
      >
        <NuxtLink 
          v-for="link in links" 
          :key="link.name" 
          :to="link.path"
          @click="isMobileOpen = false"
          class="text-3xl font-serif text-stone-900 hover:text-amber-600 transition"
        >
          {{ link.name }}
        </NuxtLink>
        <NuxtLink to="/contact" @click="isMobileOpen = false" class="mt-4">
          <button class="bg-stone-900 text-white px-10 py-4 rounded-full text-sm font-bold uppercase tracking-widest">
            Contact Us
          </button>
        </NuxtLink>
      </div>

    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isMobileOpen = ref(false)

const links = [
  { name: 'Portfolio', path: '/portfolio' },
  { name: 'Services', path: '/about' }, // Pointing to About as it contains Services info or make a dedicated page
  { name: 'About', path: '/about' }
]

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

onMounted(() => window.addEventListener('scroll', handleScroll))
onUnmounted(() => window.removeEventListener('scroll', handleScroll))
</script>