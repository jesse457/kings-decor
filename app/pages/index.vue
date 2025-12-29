<template>
  <div class="bg-background">
    <!-- Hero -->
    <AppHero />
    
    <!-- Stats Bar (Trust) -->
    <AppStats />

    <!-- Occasions (What we do) -->
    <AppOccasions />
    
    <!-- Why Choose Us (Value Prop) -->
    <AppFeatures />

    <!-- Recent Work (Visuals) -->
    <AppWorkCarousel />
    
    <!-- Testimonials (Social Proof) -->
    <AppTestimonials />

    <!-- FAQ (Information) -->
    <AppFAQ />

    <!-- Final CTA -->
    <section class="py-32 bg-primary text-primary-foreground relative overflow-hidden">
      <!-- Decorative background glow -->
      <div class="absolute top-0 right-0 w-[500px] h-[500px] bg-accent/20 blur-[120px] rounded-full pointer-events-none"></div>
      <div class="absolute bottom-0 left-0 w-[500px] h-[500px] bg-accent/20 blur-[120px] rounded-full pointer-events-none"></div>

      <div class="relative z-10 max-w-4xl mx-auto px-6 text-center">
        <span class="text-accent uppercase tracking-widest text-xs font-bold mb-4 block font-sans">Let's Create Magic</span>
        <h2 class="text-5xl md:text-7xl font-serif mb-8 leading-tight italic">Ready to Transform<br />Your Space?</h2>
        <p class="text-primary-foreground/90 text-lg mb-12 font-light max-w-2xl mx-auto font-sans">
          Whether it's a private Bed Day in Douala or a Grand Wedding in Yaoundé, 
          let's discuss how we can bring the "Kings" touch to your event.
        </p>
        <div class="flex flex-col sm:flex-row justify-center gap-6">
          <NuxtLink 
            to="/contact"
            class="w-full sm:w-auto bg-accent text-accent-foreground px-12 py-5 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-background hover:text-foreground transition-all duration-300 shadow-xl shadow-black/20 font-sans inline-block"
          >
            Get A Free Quote
          </NuxtLink>
          <a 
            href="https://wa.me/237600000000" 
            target="_blank"
            class="w-full sm:w-auto border border-primary-foreground/50 text-white px-12 py-5 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-green-600 hover:border-green-600 transition-all duration-300 flex items-center justify-center gap-2 font-sans"
            aria-label="Contact us on WhatsApp"
          >
            <span>WhatsApp Us</span>
          </a>
        </div>
      </div>
    </section>
  </div>
</template>