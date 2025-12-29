<template>
  <div>
    <AppPageHeader 
      title="The Art of Hosting" 
      subtitle="Our Philosophy"
      image="https://images.unsplash.com/photo-1556228453-efd6c1ff04f6?auto=format&fit=crop&q=80"
    />

    <!-- The Story Section -->
    <section class="py-24 px-6 max-w-7xl mx-auto grid md:grid-cols-2 gap-16 items-center">
      <div class="relative">
        <div class="aspect-[3/4] rounded-lg overflow-hidden bg-stone-200">
          <img src="https://images.unsplash.com/photo-1507652313519-d4e9174996dd?auto=format&fit=crop&q=80" class="object-cover w-full h-full" alt="Lead Decorator">
        </div>
        <!-- Decorative Box -->
        <div class="absolute -bottom-10 -right-10 w-48 h-48 bg-primary text-primary-foreground p-8 flex flex-col justify-center items-center text-center hidden md:flex rounded-2xl shadow-xl">
          <span class="text-4xl font-serif text-accent italic">12+</span>
          <span class="text-xs uppercase tracking-widest mt-2 font-sans">Years of Excellence</span>
        </div>
      </div>
      
      <div>
        <h2 class="text-4xl font-serif text-stone-900 mb-6 italic">From Douala to the World</h2>
        <p class="text-stone-600 text-lg leading-relaxed mb-6 font-sans">
          Kings Decor began with a simple belief: <span class="text-primary font-bold">Every event is a coronation.</span>
        </p>
        <p class="text-stone-500 leading-relaxed mb-8 font-sans">
          Whether we are styling a traditional "Dot" ceremony in the West, a solemn funeral service in the Center, or a modern seaside wedding in Kribi, our approach remains the same: meticulous attention to detail and a touch of royal gold.
        </p>
        <div class="grid grid-cols-2 gap-8 border-t border-stone-200 pt-8">
          <div>
            <h4 class="font-bold text-stone-900 mb-2 font-sans">Local Mastery</h4>
            <p class="text-sm text-stone-500 font-sans">We source premium flowers and wood locally, supporting Cameroonian artisans.</p>
          </div>
          <div>
            <h4 class="font-bold text-stone-900 mb-2 font-sans">Global Standard</h4>
            <p class="text-sm text-stone-500 font-sans">Our logistics team ensures punctuality and precision, rivaling international firms.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- The Process -->
    <section class="bg-stone-50 py-24">
      <div class="max-w-7xl mx-auto px-6">
        <div class="text-center mb-16">
          <h2 class="text-3xl font-serif text-stone-900 italic">How We Work</h2>
        </div>
        <div class="grid md:grid-cols-3 gap-8">
          <div class="bg-white p-10 shadow-sm border border-stone-100 group hover:-translate-y-2 transition-all duration-500 rounded-2xl">
            <span class="text-6xl font-serif text-stone-100 group-hover:text-accent/20 transition-colors">01</span>
            <h3 class="text-xl font-bold mt-4 mb-3 font-sans">Consultation</h3>
            <p class="text-stone-500 text-sm font-sans">We meet (virtually or at our Bonapriso showroom) to understand your vision, colors, and emotional tone.</p>
          </div>
          <div class="bg-white p-10 shadow-sm border border-stone-100 group hover:-translate-y-2 transition-all duration-500 rounded-2xl">
            <span class="text-6xl font-serif text-stone-100 group-hover:text-accent/20 transition-colors">02</span>
            <h3 class="text-xl font-bold mt-4 mb-3 font-sans">Concept & 3D</h3>
            <p class="text-stone-500 text-sm font-sans">We sketch the venue transformation. You see exactly how the lighting and flowers will look before the day.</p>
          </div>
          <div class="bg-white p-10 shadow-sm border border-stone-100 group hover:-translate-y-2 transition-all duration-500 rounded-2xl">
            <span class="text-6xl font-serif text-stone-100 group-hover:text-accent/20 transition-colors">03</span>
            <h3 class="text-xl font-bold mt-4 mb-3 font-sans">The Magic Day</h3>
            <p class="text-stone-500 text-sm font-sans">Our team arrives hours early. We handle setup, coordination, and tear-down. You just enjoy.</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>