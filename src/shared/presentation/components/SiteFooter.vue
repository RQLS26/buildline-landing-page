<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <footer class="site-footer" role="contentinfo">
    <div class="site-footer__grid">
      <div class="site-footer__brand">
        <img src="/assets/images/final-section/footer-brand.png" alt="BuildLine logo" class="site-footer__logo" width="248" height="84">
        <div class="site-footer__social" aria-label="Social links">
          <a href="#x" aria-label="X">
            <svg viewBox="0 0 24 24" width="28" height="28" aria-hidden="true"><use href="/assets/icons/footer-x.svg#icon"></use></svg>
          </a>
          <a href="#instagram" aria-label="Instagram">
            <svg viewBox="0 0 24 24" width="28" height="28" aria-hidden="true"><use href="/assets/icons/footer-instagram.svg#icon"></use></svg>
          </a>
          <a href="#youtube" aria-label="YouTube">
            <svg viewBox="0 0 24 24" width="28" height="28" aria-hidden="true"><use href="/assets/icons/footer-youtube.svg#icon"></use></svg>
          </a>
          <a href="#linkedin" aria-label="LinkedIn">
            <svg viewBox="0 0 24 24" width="28" height="28" aria-hidden="true"><use href="/assets/icons/footer-linkedin.svg#icon"></use></svg>
          </a>
        </div>
      </div>

      <nav class="site-footer__column" aria-label="Product links">
        <h3>Product</h3>
        <a href="#templates">Templates</a>
        <a href="#guides">Guides</a>
        <a href="#inspiration">Inspiration</a>
        <a href="#product">Product</a>
        <a href="#mobile-app">Download the Mobile app</a>
        <a href="#desktop-app">Download the Desktop app</a>
        <a href="#team-collaboration">Team collaboration</a>
      </nav>

      <nav class="site-footer__column" aria-label="Support links">
        <h3>Support</h3>
        <a href="mailto:support@gmail.com">support@gmail.com</a>
        <a href="#help-center">Help center</a>
        <a href="#pricing">Plans &amp; pricing</a>
        <a href="#upcoming">Upcoming features</a>
        <a href="#collaboration">Collaboration features</a>
        <a href="#release-notes">Release notes</a>
        <a href="#status">Application status</a>
      </nav>

      <nav class="site-footer__column" aria-label="Resources links">
        <h3>Resources</h3>
        <a href="#blog">Blog</a>
        <a href="#careers">Careers</a>
        <a href="#social">Social media</a>
        <a href="#library">Resource library</a>
        <a href="#developers">Developers</a>
        <a href="#privacy">Privacy policy</a>
        <a href="#terms">Terms of service</a>
      </nav>
    </div>
  </footer>
</template>

<style scoped>
/* Scoped styles are intentionally left empty since global styles handle the layout. */
</style>
