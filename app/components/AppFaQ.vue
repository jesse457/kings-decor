<template>
  <section class="py-24 bg-white border-t border-stone-100">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="text-4xl font-serif text-center mb-12 italic">Frequently Asked Questions</h2>
      
      <div class="space-y-4">
        <div v-for="(faq, index) in faqs" :key="index" class="border border-stone-200 rounded-lg overflow-hidden transition-all duration-300" :class="activeIndex === index ? 'shadow-md ring-1 ring-accent/20' : ''">
          <button @click="toggle(index)" class="w-full flex justify-between items-center p-6 bg-stone-50 hover:bg-stone-100 transition-all duration-300 text-left font-sans">
            <span class="font-bold text-stone-900">{{ faq.q }}</span>
            <span class="text-2xl text-accent font-light">{{ activeIndex === index ? '−' : '+' }}</span>
          </button>
          <div v-show="activeIndex === index" class="p-6 bg-white text-stone-600 text-sm leading-relaxed font-sans">
            {{ faq.a }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(0)
const faqs = [
  { q: "How far in advance should we book?", a: "For weddings, we recommend 6-12 months in advance. For Bed Days and smaller events, 1-2 months is sufficient, though availability is limited during peak seasons (December/August)." },
  { q: "Do you travel outside Douala and Yaoundé?", a: "Yes! We cover the entire national territory. We have successfully executed events in Kribi, Bafoussam, Limbe, and Bamenda. Logistics fees apply for travel." },
  { q: "Can you work with my specific budget?", a: "We have packages starting from 500,000 XAF for intimate setups. During our consultation, we tailor the design to maximize impact within your comfortable spending range." }
]

const toggle = (i) => {
  activeIndex.value = activeIndex.value === i ? null : i
}
</script>