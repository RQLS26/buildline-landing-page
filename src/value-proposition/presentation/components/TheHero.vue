<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="hero-section">
    <div class="hero-container">
      <div class="hero-content">
        <h1 class="hero-title">{{ t('hero.title') }}</h1>
        <p class="hero-subtitle">{{ t('hero.subtitle') }}</p>
        
        <div class="cta-form">
          <input type="email" :placeholder="t('hero.emailPlaceholder')" class="email-input" />
          <button class="btn-start">{{ t('hero.startFree') }}</button>
        </div>
      </div>
      
      <div class="hero-image-wrapper">
        <img src="../../../assets/hero-image.png" alt="BuildLine Dashboard Mockup" class="hero-image" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  width: 100%;
  display: flex;
  justify-content: center;
  padding: 60px 20px 80px 20px;
  background-color: #f8f9fa;
}

.hero-container {
  width: 100%;
  max-width: 1000px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: #1a1a1a;
  line-height: 1.1;
  margin-bottom: 24px;
  letter-spacing: -1px;
}

.hero-subtitle {
  font-size: 1.1rem;
  color: #666;
  line-height: 1.5;
  margin-bottom: 40px;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.cta-form {
  display: flex;
  gap: 10px;
  justify-content: center;
  margin-bottom: 60px;
}

.email-input {
  padding: 12px 20px;
  border: 1px solid #ccc;
  border-radius: 6px;
  width: 300px;
  font-size: 1rem;
  outline: none;
  font-family: inherit;
}

.email-input:focus {
  border-color: #4f86f7;
}

.btn-start {
  background-color: #4f86f7;
  color: white;
  border: none;
  border-radius: 6px;
  padding: 12px 24px;
  font-weight: 600;
  font-size: 1rem;
  transition: background-color 0.2s ease;
}

.btn-start:hover {
  background-color: #3b70db;
}

.hero-image-wrapper {
  width: 100%;
  max-width: 900px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
}

.hero-image {
  width: 100%;
  height: auto;
  border-radius: 12px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
}
</style>
