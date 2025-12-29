<template>
  <div>
    <AppPageHeader 
      title="Start Your Journey" 
      subtitle="Contact Us"
      image="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&q=80"
    />

    <section class="py-24 max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-16">
      
      <!-- Contact Info -->
      <div>
        <h2 class="text-4xl font-serif text-stone-900 mb-8">Visit our Showrooms</h2>
        
        <div class="space-y-10">
          <div class="flex gap-6">
            <div class="w-12 h-12 bg-amber-100 text-amber-600 flex items-center justify-center rounded-full shrink-0">
              <span class="font-bold text-xl">D</span>
            </div>
            <div>
              <h3 class="text-xl font-bold mb-2">Douala (HQ)</h3>
              <p class="text-stone-500">Rue des Palmiers, Bonapriso<br>Immeuble Kings, 2nd Floor</p>
              <a href="tel:+237600000000" class="inline-block mt-2 text-stone-900 font-semibold border-b border-stone-300 hover:border-amber-600">677-00-00-00</a>
            </div>
          </div>

          <div class="flex gap-6">
            <div class="w-12 h-12 bg-stone-100 text-stone-600 flex items-center justify-center rounded-full shrink-0">
              <span class="font-bold text-xl">Y</span>
            </div>
            <div>
              <h3 class="text-xl font-bold mb-2">Yaoundé</h3>
              <p class="text-stone-500">Avenue Bastos, Near Embassy Area<br>Villa 45</p>
              <a href="tel:+237600000000" class="inline-block mt-2 text-stone-900 font-semibold border-b border-stone-300 hover:border-amber-600">699-00-00-00</a>
            </div>
          </div>
        </div>

        <div class="mt-12 p-8 bg-green-50 rounded-2xl border border-green-100">
          <h4 class="text-green-800 font-bold mb-2">Fast Response?</h4>
          <p class="text-green-700 text-sm mb-4">For urgent event inquiries, WhatsApp is the fastest way to reach our styling team.</p>
          <button class="bg-green-600 text-white px-6 py-3 rounded-full font-bold text-sm hover:bg-green-700 transition w-full md:w-auto">
            Chat on WhatsApp
          </button>
        </div>
      </div>

      <!-- Form -->
      <div class="bg-white p-10 shadow-xl rounded-2xl border border-stone-100">
        <h3 class="text-2xl font-serif mb-6">Send us a message</h3>
        <form class="space-y-6">
          <div class="grid md:grid-cols-2 gap-6">
            <div>
              <label class="block text-xs font-bold uppercase tracking-widest text-stone-500 mb-2">First Name</label>
              <input type="text" class="w-full bg-stone-50 border border-stone-200 p-3 focus:outline-none focus:border-amber-500 transition" />
            </div>
            <div>
              <label class="block text-xs font-bold uppercase tracking-widest text-stone-500 mb-2">Last Name</label>
              <input type="text" class="w-full bg-stone-50 border border-stone-200 p-3 focus:outline-none focus:border-amber-500 transition" />
            </div>
          </div>

          <div>
            <label class="block text-xs font-bold uppercase tracking-widest text-stone-500 mb-2">Event Type</label>
            <select class="w-full bg-stone-50 border border-stone-200 p-3 focus:outline-none focus:border-amber-500 transition text-stone-700">
              <option>Wedding</option>
              <option>Bed Day (Newborn/Bride)</option>
              <option>Funeral / Memorial</option>
              <option>Corporate Event</option>
              <option>Other</option>
            </select>
          </div>

          <div>
            <label class="block text-xs font-bold uppercase tracking-widest text-stone-500 mb-2">Your Vision</label>
            <textarea rows="4" class="w-full bg-stone-50 border border-stone-200 p-3 focus:outline-none focus:border-amber-500 transition"></textarea>
          </div>

          <button class="w-full bg-stone-900 text-white py-4 font-bold uppercase tracking-widest text-xs hover:bg-amber-600 transition duration-300">
            Send Inquiry
          </button>
        </form>
      </div>

    </section>
  </div>
</template>