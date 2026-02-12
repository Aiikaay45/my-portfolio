<script setup>
  import NavBar from '@/components/NavBar.vue';
  import HeroSection from './components/HeroSection.vue';
import { defineAsyncComponent } from 'vue';
import ServicesSection from './components/ServicesSection.vue';
import AboutSection from './components/AboutSection.vue';
import ExperienceAndSkills from './components/ExperienceAndSkills.vue';
import LatestProjSection from './components/LatestProjSection.vue';
import ContactSection from './components/ContactSection.vue';
import TestimonialsSection from './components/TestimonialsSection.vue';
import Footer from './components/Footer.vue';
import BackToTop from './components/BackToTop.vue';
//import HeroSection from './components/HeroSection.vue';
//const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar />
    <HeroSection />
    <ServicesSection />
    <AboutSection />
    <ExperienceAndSkills />
    <LatestProjSection />
    <ContactSection />
    <TestimonialsSection />
    <Footer />
    <BackToTop />
  </div>
</template>

