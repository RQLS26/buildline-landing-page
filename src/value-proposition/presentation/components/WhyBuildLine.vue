<script setup>
import { useI18n } from 'vue-i18n'
import { onMounted } from 'vue'

const { t } = useI18n()

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          // Use existing CSS classes from layout.css
          if (entry.target.classList.contains('why-section__header')) {
            entry.target.classList.add('why-section__header--visible')
          } else if (entry.target.classList.contains('why-card')) {
            entry.target.classList.add('why-card--visible')
          }
        }
      })
    },
    { threshold: 0.15 }
  )

  const header = document.querySelector('#why .why-section__header')
  if (header) {
    header.classList.add('why-section__header--motion')
    observer.observe(header)
  }

  document.querySelectorAll('#why .why-card').forEach((card) => {
    card.classList.add('why-card--motion')
    observer.observe(card)
  })
})
</script>

<template>
  <section id="why" class="why-section" aria-labelledby="why-title">
    <header class="why-section__header">
      <h2 id="why-title">Why BuildLine?</h2>
      <p class="why-section__subtitle">
        Designed for project managers, logistics teams, and site engineers to manage procurement, materials, and project costs efficiently.
      </p>
    </header>

    <div class="why-grid">
      <article class="why-card">
        <span class="why-card__quote-mark" aria-hidden="true">&ldquo;</span>
        <p class="why-card__quote">It's simple, mobile, and focused on preventing money from being lost in logistics.</p>
        <img class="why-card__avatar" src="/assets/images/testimonials/avatar-1.png" alt="Daniel Reyes" loading="lazy" decoding="async">
        <p class="why-card__role">Store Owner</p>
        <p class="why-card__name">Daniel Reyes</p>
      </article>

      <article class="why-card">
        <span class="why-card__quote-mark" aria-hidden="true">&ldquo;</span>
        <p class="why-card__quote">Eliminating manual Excel spreadsheets drastically reduced administrative stress for the team.</p>
        <img class="why-card__avatar" src="/assets/images/testimonials/avatar-2.png" alt="Laura Mendoza" loading="lazy" decoding="async">
        <p class="why-card__role">Market Supervisor</p>
        <p class="why-card__name">Laura Mendoza</p>
      </article>

      <article class="why-card">
        <span class="why-card__quote-mark" aria-hidden="true">&ldquo;</span>
        <p class="why-card__quote">Buildline centralized our suppliers. What used to take 48 hours to quote, we now resolve in a morning.</p>
        <img class="why-card__avatar" src="/assets/images/testimonials/avatar-3.png" alt="Andrés Silva" loading="lazy" decoding="async">
        <p class="why-card__role">Operations Manager</p>
        <p class="why-card__name">Andrés Silva</p>
      </article>

      <article class="why-card">
        <span class="why-card__quote-mark" aria-hidden="true">&ldquo;</span>
        <p class="why-card__quote">Remote approval is key. I can validate purchase orders from the field without having to return to the office.</p>
        <img class="why-card__avatar" src="/assets/images/testimonials/avatar-4.png" alt="Ricardo Torres" loading="lazy" decoding="async">
        <p class="why-card__role">Quality Manager</p>
        <p class="why-card__name">Ricardo Torres</p>
      </article>

      <article class="why-card">
        <span class="why-card__quote-mark" aria-hidden="true">&ldquo;</span>
        <p class="why-card__quote">Visualizing actual spending versus budget in real time has allowed us to preserve the project's profit margin.</p>
        <img class="why-card__avatar" src="/assets/images/testimonials/avatar-5.png" alt="Sofia Rojas" loading="lazy" decoding="async">
        <p class="why-card__role">Logistics Coordinator</p>
        <p class="why-card__name">Sofia Rojas</p>
      </article>

      <article class="why-card">
        <span class="why-card__quote-mark" aria-hidden="true">&ldquo;</span>
        <p class="why-card__quote">We've finally stopped approving purchases via WhatsApp. Order errors have dropped to zero.</p>
        <img class="why-card__avatar" src="/assets/images/testimonials/avatar-6.png" alt="Jorge Castillo" loading="lazy" decoding="async">
        <p class="why-card__role">Compliance Director</p>
        <p class="why-card__name">Jorge Castillo</p>
      </article>
    </div>
  </section>
</template>

<style scoped>
/* Scoped styles are intentionally left empty since global styles handle the layout. */
</style>
