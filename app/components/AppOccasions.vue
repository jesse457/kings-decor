<template>
  <section class="py-32 px-6 md:px-12 bg-background">
    <div class="max-w-7xl mx-auto">
      
      <!-- Section Header -->
      <div class="flex flex-col md:flex-row justify-between items-end mb-16 border-b border-border pb-8">
        <div>
          <h2 class="text-4xl md:text-6xl font-serif text-foreground mb-4 italic">Curated Occasions</h2>
          <p class="text-muted-foreground max-w-md font-sans">We understand the cultural significance of every gathering in Cameroon.</p>
        </div>
        <div class="hidden md:block text-right">
          <p class="text-xs uppercase tracking-widest text-muted-foreground font-sans">Kings Decor Signatures</p>
        </div>
      </div>

      <!-- The Trio Grid -->
      <div class="grid md:grid-cols-3 gap-4">
        
        <!-- 1. Bed Days -->
        <div class="group relative h-[600px] overflow-hidden rounded-2xl cursor-pointer bg-card">
          <img 
            src="https://images.unsplash.com/photo-1616593871241-c75c589d97b5?q=80&w=2070&auto=format&fit=crop" 
            alt="Luxurious bedroom setup for Bed Days"
            class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
          />
          <div class="absolute inset-0 bg-black/40 group-hover:bg-black/60 transition-colors"></div>
          <div class="absolute bottom-0 left-0 p-8 w-full">
            <h3 class="text-3xl font-serif text-white mb-2 italic">Bed Days</h3>
            <p class="text-stone-200 text-sm opacity-0 translate-y-4 group-hover:opacity-100 group-hover:translate-y-0 transition-all duration-500 font-sans">
              Transforming the intimate space for the bride or newborn with luxurious linens, soft lighting, and floral elegance.
            </p>
          </div>
        </div>

        <!-- 2. Funerals -->
        <div class="group relative h-[600px] overflow-hidden rounded-2xl cursor-pointer bg-card">
          <img 
            src="https://images.unsplash.com/photo-1596525727632-6a6873321528?q=80&w=2072&auto=format&fit=crop" 
            alt="Dignified memorial service setup"
            class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0"
          />
          <div class="absolute inset-0 bg-black/50 group-hover:bg-black/70 transition-colors"></div>
          <div class="absolute bottom-0 left-0 p-8 w-full">
            <h3 class="text-3xl font-serif text-white mb-2 italic">Memorials & Funerals</h3>
            <p class="text-stone-200 text-sm opacity-0 translate-y-4 group-hover:opacity-100 group-hover:translate-y-0 transition-all duration-500 font-sans">
              Honoring a life well-lived with dignified, majestic setups. From the lying-in-state to the final reception.
            </p>
          </div>
        </div>

        <!-- 3. Weddings -->
        <div class="group relative h-[600px] overflow-hidden rounded-2xl cursor-pointer bg-card">
          <img 
            src="https://images.unsplash.com/photo-1519225421980-715cb0202128?q=80&w=1500&auto=format&fit=crop" 
            alt="Grand wedding reception setup"
            class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
          />
          <div class="absolute inset-0 bg-black/40 group-hover:bg-black/60 transition-colors"></div>
          <div class="absolute bottom-0 left-0 p-8 w-full">
            <h3 class="text-3xl font-serif text-white mb-2 italic">Royal Weddings</h3>
            <p class="text-stone-200 text-sm opacity-0 translate-y-4 group-hover:opacity-100 group-hover:translate-y-0 transition-all duration-500 font-sans">
              Complete venue transformation. Centerpieces, stages, and lighting that leave your guests breathless.
            </p>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>