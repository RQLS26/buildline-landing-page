<script setup>
import { useI18n } from 'vue-i18n'
import { onMounted } from 'vue'

const { t } = useI18n()

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-revealed')
        }
      })
    },
    { threshold: 0.15 }
  )
  document.querySelectorAll('[data-reveal]').forEach((el) => observer.observe(el))
})
</script>

<template>
  <section id="features" aria-labelledby="features-title">
    <header class="section-header section-header--features" data-reveal>
      <h2 id="features-title">
        Everything you need to manage and optimize
      </h2>
      <p class="section-header__lead">
        Project blueprints, real-time dashboards, automated notifications, and compliance reports — no manual spreadsheets, no lost purchase orders, no surprises.
      </p>
    </header>

    <div class="feature-diagram">
      <!-- 01 · Planning -->
      <article class="feature-step feature-step--monitoring" data-reveal="scale-in" style="--reveal-delay: 0ms">
        <span class="feature-step__eyebrow feature-step__eyebrow--blue">01 · Planning</span>
        <h3 class="feature-step__title">Real-time project planning & tracking</h3>
        <div class="feature-step__art" aria-hidden="true">
          <img class="feature-illustration" src="/assets/images/features/sketch.png" alt="">
        </div>
        <p class="feature-step__body">Budget allocation, material schedules, and workforce tasks tracked live across all your active construction sites.</p>
      </article>

      <div class="feature-note feature-note--history" data-reveal="fade-left" style="--reveal-delay: 150ms">
        <svg class="feature-note__arrow" viewBox="0 0 120 118" aria-hidden="true"><use href="/assets/icons/feature-arrow.svg#icon"></use></svg>
        <p class="feature-note__copy">Export your project history by site, phase, or period</p>
      </div>

      <!-- 02 · Records -->
      <article class="feature-step feature-step--records" data-reveal="slide-stack">
        <span class="feature-step__eyebrow feature-step__eyebrow--orange">02 · Records</span>
        <h3 class="feature-step__title">Download your complete history</h3>
        <div class="feature-step__art" aria-hidden="true">
          <img class="feature-illustration" src="/assets/images/features/report.png" alt="">
        </div>
        <p class="feature-step__body">Every transaction is logged and exportable. Download procurement data by supplier, by site, or by period, in CSV or PDF format.</p>
      </article>

      <div class="feature-note feature-note--records" data-reveal="fade-left" style="--reveal-delay: 250ms">
        <svg class="feature-note__arrow" viewBox="0 0 120 118" aria-hidden="true"><use href="/assets/icons/feature-arrow.svg#icon"></use></svg>
        <p class="feature-note__copy">Download records by material type or supplier</p>
      </div>

      <!-- 03 · Alerts -->
      <article class="feature-step feature-step--alerts" data-reveal="slide-stack">
        <span class="feature-step__eyebrow feature-step__eyebrow--red">03 · Alerts</span>
        <h3 class="feature-step__title">Notifications the moment something deviates</h3>
        <div class="feature-step__art" aria-hidden="true">
          <img class="feature-illustration" src="/assets/images/features/new-email.png" alt="">
        </div>
        <p class="feature-step__body">Email and messaging alerts when costs exceed budgets or deliveries are delayed. The project manager is notified instantly.</p>
      </article>

      <div class="feature-note feature-note--incidents" data-reveal="fade-left" style="--reveal-delay: 350ms">
        <svg class="feature-note__arrow" viewBox="0 0 120 118" aria-hidden="true"><use href="/assets/icons/feature-arrow.svg#icon"></use></svg>
        <p class="feature-note__copy">Download alert and incident logs instantly</p>
      </div>

      <!-- 04 · Compliance -->
      <article class="feature-step feature-step--compliance" data-reveal="slide-stack">
        <span class="feature-step__eyebrow feature-step__eyebrow--green">04 · Compliance</span>
        <h3 class="feature-step__title">Audit-ready reports & documentation</h3>
        <div class="feature-step__art" aria-hidden="true">
          <img class="feature-illustration" src="/assets/images/features/audit.png" alt="">
        </div>
        <p class="feature-step__body">Inspection reports and logs exportable in one click. Ready-to-use templates for regulatory submissions and safety audits.</p>
      </article>

      <!-- Benefits aside -->
      <aside class="feature-benefits" data-reveal="fade-right">
        <span class="feature-benefits__label">More benefits for you</span>
        <div class="feature-benefit">
          <svg class="feature-benefit__icon" viewBox="0 0 56 56" aria-hidden="true"><use href="/assets/icons/benefit-clock.svg#icon"></use></svg>
          <p class="feature-benefit__text">
            <span class="feature-benefit__highlight">Save time:</span>
            <span>automate tasks and eliminate manual records.</span>
          </p>
        </div>
        <div class="feature-benefit">
          <svg class="feature-benefit__icon" viewBox="0 0 56 56" aria-hidden="true"><use href="/assets/icons/benefit-warning.svg#icon"></use></svg>
          <p class="feature-benefit__text">
            <span class="feature-benefit__highlight">Reduce risks:</span>
            <span>act early and prevent incidents before they happen.</span>
          </p>
        </div>
      </aside>
    </div>
  </section>
</template>

<style scoped>
/* Scoped styles are intentionally left empty since global styles handle the layout. */
</style>
