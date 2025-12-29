<template>
  <nav 
    class="fixed top-0 w-full z-50 transition-all duration-500 border-b"
    :class="[
      isScrolled || isMobileOpen 
        ? 'bg-background/90 backdrop-blur-md py-4 border-border shadow-sm text-foreground' 
        : 'bg-transparent py-5 border-transparent text-white'
    ]"
    role="navigation"
    aria-label="Main Navigation"
  >
    <div class="max-w-7xl mx-auto px-6 flex items-center justify-between">
      
      <!-- Logo -->
      <NuxtLink to="/" class="relative z-50 flex items-center gap-2 group" aria-label="Home">
        <span class="text-2xl font-serif font-bold tracking-tighter uppercase transition-colors duration-300">
          Kings<span class="text-accent">.</span>
        </span>
      </NuxtLink>

      <!-- Desktop Links -->
      <div class="hidden md:flex gap-8 items-center" role="menubar">
        <NuxtLink 
          v-for="link in links" 
          :key="link.name" 
          :to="link.path"
          role="menuitem"
          class="text-xs font-bold uppercase tracking-[0.15em] font-sans hover:text-accent transition-colors duration-300 relative after:content-[''] after:absolute after:-bottom-2 after:left-0 after:w-0 after:h-[2px] after:bg-accent after:transition-all after:duration-300 hover:after:w-full"
        >
          {{ link.name }}
        </NuxtLink>
      </div>

      <!-- Desktop CTA -->
      <div class="hidden md:block">
        <NuxtLink 
          to="/contact"
          class="inline-block px-8 py-3 rounded-full text-xs font-bold uppercase tracking-widest transition-all duration-300 border font-sans"
          :class="isScrolled ? 'bg-primary text-primary-foreground border-primary hover:bg-accent hover:border-accent hover:text-accent-foreground' : 'bg-background text-foreground border-background hover:bg-muted'"
        >
          Book Now
        </NuxtLink>
      </div>

      <!-- Mobile Hamburger -->
      <button 
        @click="toggleMobileMenu" 
        class="md:hidden z-50 relative w-10 h-10 flex items-center justify-center focus:outline-none"
        :aria-expanded="isMobileOpen"
        aria-label="Toggle Menu"
      >
        <div class="w-6 flex flex-col items-end gap-1.5 transition-all duration-300">
          <span 
            class="h-[2px] w-full bg-current transition-all duration-300 origin-center"
            :class="isMobileOpen ? 'rotate-45 translate-y-2' : ''"
          ></span>
          <span 
            class="h-[2px] w-full bg-current transition-all duration-300"
            :class="isMobileOpen ? 'opacity-0' : ''"
          ></span>
          <span 
            class="h-[2px] w-full bg-current transition-all duration-300 origin-center"
            :class="isMobileOpen ? '-rotate-45 -translate-y-2' : ''"
          ></span>
        </div>
      </button>

      <!-- Mobile Overlay Menu -->
      <div 
        class="fixed inset-0 bg-background z-40 flex flex-col pt-32 px-8 gap-8 transition-all duration-500 md:hidden"
        :class="isMobileOpen ? 'translate-x-0 opacity-100' : 'translate-x-full opacity-0'"
        :aria-hidden="!isMobileOpen"
      >
        <div class="flex flex-col gap-6">
          <NuxtLink 
            v-for="link in links" 
            :key="link.name" 
            :to="link.path"
            @click="toggleMobileMenu"
            class="text-4xl font-serif text-foreground hover:text-accent hover:pl-4 transition-all duration-300 border-b border-border pb-4"
          >
            {{ link.name }}
          </NuxtLink>
        </div>

        <div class="mt-auto mb-12">
          <p class="text-muted-foreground text-xs uppercase tracking-widest mb-4 font-sans">Contact</p>
          <p class="text-xl font-serif text-foreground">+237 677 00 00 00</p>
          <p class="text-muted-foreground mt-2 font-sans">Bonapriso, Douala</p>
          
          <NuxtLink 
            to="/contact" 
            @click="toggleMobileMenu" 
            class="mt-8 block w-full bg-primary text-primary-foreground py-4 rounded-full font-bold uppercase tracking-widest text-xs font-sans text-center"
          >
            Get Quote
          </NuxtLink>
        </div>
      </div>

    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted, watch } from 'vue'

const isScrolled = ref(false)
const isMobileOpen = ref(false)

const links = [
  { name: 'Home', path: '/' },
  { name: 'Portfolio', path: '/portfolio' },
  { name: 'Services', path: '/services' }, // Consolidated into services page
  { name: 'About', path: '/about' },
  { name: 'Contact', path: '/contact' }
]

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20
}

const toggleMobileMenu = () => {
  isMobileOpen.value = !isMobileOpen.value
}

// Lock body scroll when mobile menu is open
watch(isMobileOpen, (val) => {
  if (val) {
    document.body.style.overflow = 'hidden'
  } else {
    document.body.style.overflow = ''
  }
})

onMounted(() => window.addEventListener('scroll', handleScroll))
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
  document.body.style.overflow = '' // Ensure cleanup
})
</script>