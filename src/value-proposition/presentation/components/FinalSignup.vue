<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section id="contact" class="signup-shell" aria-labelledby="contact-title">
    <div class="signup-shell__stage">
      <img class="signup-shell__art signup-shell__art--left" src="/assets/images/final-section/signup-art-left.png" alt="" loading="eager" decoding="async">
      <img class="signup-shell__art signup-shell__art--right" src="/assets/images/final-section/signup-art-right.png" alt="" loading="eager" decoding="async">

      <form class="signup-card" novalidate>
        <h2 id="contact-title" class="signup-card__title">Create Account now</h2>
        <p class="signup-card__subtitle">Start monitoring now</p>

        <div class="signup-field">
          <label for="first-name">Your name</label>
          <div class="signup-card__split">
            <input id="first-name" class="input" type="text" autocomplete="given-name" placeholder="First name">
            <input id="last-name" class="input" type="text" autocomplete="family-name" placeholder="Last name">
          </div>
        </div>

        <div class="signup-field">
          <label for="signup-email">Your email address</label>
          <input id="signup-email" class="input" type="email" autocomplete="email" placeholder="example_123@email.com">
        </div>

        <div class="signup-field">
          <label for="signup-password">Choose a password</label>
          <div class="signup-password">
            <input id="signup-password" class="input" type="password" autocomplete="new-password" placeholder="........">
            <button type="button" class="signup-password__toggle" aria-label="Show password">
              <svg viewBox="0 0 24 24" width="22" height="22" aria-hidden="true"><use href="/assets/icons/signup-eye-off.svg#icon"></use></svg>
            </button>
          </div>
        </div>

        <button type="submit" class="btn signup-card__submit">Summit</button>

        <p class="signup-card__terms">
          <span>By creating your account, you agree to the </span>
          <span><a href="#terms">Terms</a> and <a href="#conditions">Conditions</a>.</span>
        </p>

        <div class="signup-card__divider">
          <span>or sign up with</span>
        </div>

        <div class="signup-card__social">
          <a href="#google" class="signup-card__social-btn signup-card__social-btn--google">
            <span class="signup-card__social-icon signup-card__social-icon--google" aria-hidden="true">
              <svg viewBox="0 0 24 24" width="26" height="26"><use href="/assets/icons/signup-google.svg#icon"></use></svg>
            </span>
            <span>Sign up with Google</span>
          </a>

          <a href="#apple" class="signup-card__social-btn signup-card__social-btn--apple">
            <span class="signup-card__social-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" width="26" height="26"><use href="/assets/icons/signup-apple.svg#icon"></use></svg>
            </span>
            <span>Sign up with Apple</span>
          </a>
        </div>
      </form>
    </div>
  </section>
</template>

<style scoped>
/* Scoped styles are intentionally left empty since global styles handle the layout. */
</style>
