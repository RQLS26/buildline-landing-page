<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <header class="site-header" role="banner">
    <nav class="navbar" aria-label="Main navigation">
      <a href="#home" class="navbar__logo" aria-label="BuildLine home">
        <img src="/assets/images/logo/coldtrace-logo.png" alt="BuildLine logo" width="228" height="72">
      </a>

      <button type="button" class="navbar__more" aria-label="Open navigation menu" aria-controls="mobile-nav-panel" aria-expanded="false">
        <svg viewBox="0 0 24 24" width="24" height="24" aria-hidden="true"><use href="/assets/icons/navbar-more.svg#icon"></use></svg>
        <span>{{ t('nav.product') }}</span> <!-- Placeholder for 'More' text -->
      </button>

      <ul class="navbar__menu">
        <li><a href="#products" class="nav-pill nav-pill--active">Products</a></li>
        <li><a href="#solutions" class="nav-pill nav-pill--active">Solutions</a></li>
        <li><a href="#community" class="nav-pill">Community</a></li>
        <li><a href="#resources" class="nav-pill">Resources</a></li>
        <li><a href="#pricing" class="nav-pill">Pricing</a></li>
        <li><a href="#contact" class="nav-pill">Contact</a></li>
      </ul>

      <div class="navbar__actions">
        <a href="#signin" class="btn" style="background-color: #E3E3E3; color: #333; padding: 0 20px;">Sign in</a>
        <a href="#register" class="btn btn--primary" style="background-color: #6798EE; border-color: #6798EE;">Register now</a>
      </div>

      <div class="navbar__mobile-menu" id="mobile-nav-panel" hidden>
        <div class="navbar__mobile-links" aria-label="Mobile navigation">
          <a href="#home" class="navbar__mobile-link">{{ t('nav.product') }}</a>
          <a href="#features" class="navbar__mobile-link">{{ t('nav.solutions') }}</a>
          <a href="#pricing" class="navbar__mobile-link">{{ t('nav.pricing') }}</a>
          <a href="#resources" class="navbar__mobile-link">{{ t('nav.resources') }}</a>
        </div>

        <div class="navbar__mobile-language">
          <p class="navbar__mobile-language-title">Language</p>
          <div class="lang-switcher lang-switcher--mobile" role="group" aria-label="Select language">
            <button type="button" class="lang-switcher__option is-active" @click="$i18n.locale = 'en'" aria-pressed="true">EN</button>
            <button type="button" class="lang-switcher__option" @click="$i18n.locale = 'es'" aria-pressed="false">ES</button>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped>
/* Scoped styles are intentionally left empty since global styles handle the layout. */
</style>
