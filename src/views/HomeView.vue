<script setup>
import HeroSection from '../components/sections/HeroSection.vue'
import SponsorSection from '../components/sections/SponsorSection.vue'
import FeaturesSection from '../components/sections/FeaturesSection.vue'
import HowItWorksSection from '../components/sections/HowItWorksSection.vue'
import TestimonialsSection from '../components/sections/TestimonialsSection.vue'
import PricingSection from '../components/sections/PricingSection.vue'
import FAQSection from '../components/sections/FAQSection.vue'
import CTASection from '../components/sections/CTASection.vue'
import ContactSection from '../components/sections/ContactSection.vue'
</script>

<template>
  <div class="home-view">
    <!-- Hero Section -->
    <HeroSection />
    
    <!-- Sponsor Infinite Scroll Strip -->
    <SponsorSection />
    
    <!-- Divider accent line -->
    <div class="divider-accent"></div>

    <!-- Features Section -->
    <FeaturesSection />

    <!-- How It Works Section -->
    <HowItWorksSection />

    <!-- Divider accent line -->
    <div class="divider-accent"></div>

    <!-- Testimonials Section -->
    <TestimonialsSection />

    <!-- Pricing Section -->
    <PricingSection />

    <!-- FAQ Section -->
    <FAQSection />

    <!-- CTA Section -->
    <CTASection />

    <!-- Contact Section -->
    <ContactSection />
  </div>
</template>

<style scoped>
.home-view {
  overflow-x: hidden;
}

/* Subtle brand colored gradient divider lines */
.divider-accent {
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent 0%, rgba(124, 58, 237, 0.15) 50%, transparent 100%);
}
</style>
