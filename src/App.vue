<template>
  <div class="bg-[#25579d] min-h-screen">

     <Suspense>
      <template #default>
        
         <div>
            <XinChao />
            <NavBar />
            <HeroSection />
            <ServicesSection />
            <Exprience />
            
            <LatestProjSection />
            <ContactSection />

            <Footer />
            <BackToTop />
      </div>
    </template>
    <template #fallback>
      <div class="flex justify-center items-center min-h-screen">
          <loadingSpinner />
      </div>
    </template>
  </Suspense>
  </div>
</template>

<script setup>
 import { defineAsyncComponent } from 'vue';
//Import Components Asynchronously
const XinChao = defineAsyncComponent(()=>import('@/components/XinChao.vue'));
const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const HeroSection = defineAsyncComponent(()=>import('@/components/HeroSection.vue'));
const ServicesSection = defineAsyncComponent(()=>import('@/components/ServicesSection.vue'));
const LatestProjSection = defineAsyncComponent(()=>import('@/components/LatestProjSection.vue'));
const ContactSection = defineAsyncComponent(()=>import('@/components/ContactSection.vue'));
const Footer = defineAsyncComponent(()=>import('@/components/Footer.vue'));
const BackToTop = defineAsyncComponent(()=>import('@/components/BackToTop.vue'));
import loadingSpinner from './components/loadingSpinner.vue';
import Exprience from './components/Exprience.vue';
</script>
<style>

*{
  scrollbar-width: thin;
  scrollbar-color: #a5d8f1 #f1f1f1;
}
body, html {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}
</style>

