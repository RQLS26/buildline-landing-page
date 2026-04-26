<script setup>
import TheHeader from './shared/presentation/components/TheHeader.vue'
import TheHero from './value-proposition/presentation/components/TheHero.vue'
import AppFeatures from './value-proposition/presentation/components/AppFeatures.vue'
import ProductShowcase from './value-proposition/presentation/components/ProductShowcase.vue'
import WhyBuildLine from './value-proposition/presentation/components/WhyBuildLine.vue'
</script>

<template>
  <div class="landing-page">
    <TheHeader />
    <main>
      <TheHero />
      <AppFeatures />
      <ProductShowcase />
      <WhyBuildLine />
      <!-- We will add more sections here -->
    </main>
  </div>
</template>

<style scoped>
.landing-page {
  font-family: 'Inter', sans-serif;
  color: #333;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

main {
  /* Offset removed to fix white gap */
}
</style>
