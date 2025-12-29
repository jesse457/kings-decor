<template>
  <section class="py-24 bg-background overflow-hidden relative">
    <!-- Decorative Quote Icon -->
    <div class="absolute top-10 left-10 text-muted/20 font-serif text-[200px] leading-none select-none -z-0">"</div>

    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="flex flex-col md:flex-row justify-between items-end mb-16">
        <h2 class="text-4xl font-serif text-foreground italic">Love Letters</h2>
        <div class="flex gap-2 mt-4 md:mt-0">
          <button class="w-12 h-12 flex items-center justify-center border border-border rounded-full hover:bg-primary hover:text-primary-foreground transition-all duration-300" aria-label="Previous testimonial">←</button>
          <button class="w-12 h-12 flex items-center justify-center border border-border rounded-full hover:bg-primary hover:text-primary-foreground transition-all duration-300" aria-label="Next testimonial">→</button>
        </div>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Review 1 -->
        <div class="bg-card p-8 rounded-xl border border-border shadow-sm">
          <div class="flex gap-1 text-accent mb-4">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <p class="text-muted-foreground italic mb-6 font-serif">"My Bed Day was exactly what I dreamed of. Kings Decor transformed my small living room into a palace. The lighting was magical."</p>
          <div class="flex items-center gap-4">
            <div class="w-10 h-10 bg-muted rounded-full overflow-hidden">
               <img src="https://i.pravatar.cc/100?img=5" alt="Sarah M." class="w-full h-full object-cover">
            </div>
            <div>
              <h4 class="font-bold text-sm text-foreground font-sans">Sarah M.</h4>
              <p class="text-xs text-muted-foreground font-sans">Douala</p>
            </div>
          </div>
        </div>

        <!-- Review 2 -->
        <div class="bg-primary text-primary-foreground p-8 rounded-xl shadow-xl transform md:-translate-y-4">
          <div class="flex gap-1 text-accent mb-4">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <p class="text-primary-foreground/90 italic mb-6 font-serif">"Professionalism is rare in this industry, but these guys have it. They handled our wedding of 500 guests in Yaoundé flawlessly."</p>
          <div class="flex items-center gap-4">
            <div class="w-10 h-10 bg-background/20 rounded-full overflow-hidden">
               <img src="https://i.pravatar.cc/100?img=12" alt="Jean-Paul K." class="w-full h-full object-cover">
            </div>
            <div>
              <h4 class="font-bold text-sm text-primary-foreground font-sans">Jean-Paul K.</h4>
              <p class="text-xs text-primary-foreground/70 font-sans">Yaoundé</p>
            </div>
          </div>
        </div>

        <!-- Review 3 -->
        <div class="bg-card p-8 rounded-xl border border-border shadow-sm">
          <div class="flex gap-1 text-accent mb-4">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <p class="text-muted-foreground italic mb-6 font-serif">"They honored my late father with a funeral setup that was dignified and royal. It brought peace to the whole family."</p>
          <div class="flex items-center gap-4">
            <div class="w-10 h-10 bg-muted rounded-full overflow-hidden">
               <img src="https://i.pravatar.cc/100?img=3" alt="Marie T." class="w-full h-full object-cover">
            </div>
            <div>
              <h4 class="font-bold text-sm text-foreground font-sans">Marie T.</h4>
              <p class="text-xs text-muted-foreground font-sans">Bafoussam</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>