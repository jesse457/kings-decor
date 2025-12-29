<template>
  <footer class="bg-stone-950 text-white pt-20 pb-8">
    <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-4 gap-12 border-b border-stone-800 pb-16">
      
      <!-- Brand -->
      <div class="md:col-span-1">
        <div class="text-2xl font-serif font-bold tracking-tighter uppercase mb-6">
          Kings<span class="text-amber-500">.</span>
        </div>
        <p class="text-stone-400 text-sm leading-relaxed">
          Elevating life's most significant moments with Cameroonian elegance and international luxury standards.
        </p>
      </div>

      <!-- Quick Links -->
      <div>
        <h4 class="text-amber-500 text-xs font-bold uppercase tracking-widest mb-6">Explore</h4>
        <ul class="space-y-4 text-sm text-stone-400">
          <li><NuxtLink to="/about" class="hover:text-white transition">The Kings Story</NuxtLink></li>
          <li><NuxtLink to="/portfolio" class="hover:text-white transition">Our Portfolio</NuxtLink></li>
          <li><NuxtLink to="/services" class="hover:text-white transition">Services</NuxtLink></li>
          <li><NuxtLink to="/contact" class="hover:text-white transition">Book Consultation</NuxtLink></li>
        </ul>
      </div>

      <!-- Services -->
      <div>
        <h4 class="text-amber-500 text-xs font-bold uppercase tracking-widest mb-6">Occasions</h4>
        <ul class="space-y-4 text-sm text-stone-400">
          <li>Wedding Design</li>
          <li>Traditional Dot</li>
          <li>Bed Days (Newborns)</li>
          <li>Funeral Honors</li>
          <li>Corporate Galas</li>
        </ul>
      </div>

      <!-- Contact -->
      <div>
        <h4 class="text-amber-500 text-xs font-bold uppercase tracking-widest mb-6">Contact</h4>
        <ul class="space-y-4 text-sm text-stone-400">
          <li>Bonapriso, Douala</li>
          <li>Bastos, Yaoundé</li>
          <li>(+237) 677-00-00-00</li>
          <li>hello@kingsdecor.cm</li>
        </ul>
        <div class="flex gap-4 mt-6">
          <!-- Social Icons (Placeholders) -->
          <div class="w-8 h-8 rounded-full bg-stone-800 flex items-center justify-center hover:bg-amber-600 transition cursor-pointer">IG</div>
          <div class="w-8 h-8 rounded-full bg-stone-800 flex items-center justify-center hover:bg-amber-600 transition cursor-pointer">FB</div>
        </div>
      </div>
    </div>

    <div class="max-w-7xl mx-auto px-6 pt-8 flex flex-col md:flex-row justify-between items-center text-xs text-stone-600">
      <p>&copy; 2025 Kings Decor Cameroon.</p>
      <div class="flex gap-6 mt-4 md:mt-0">
        <a href="#">Privacy Policy</a>
        <a href="#">Terms of Service</a>
      </div>
    </div>
  </footer>
</template>