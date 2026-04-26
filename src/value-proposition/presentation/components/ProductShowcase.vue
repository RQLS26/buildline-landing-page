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
    { threshold: 0.12 }
  )
  document.querySelectorAll('#about-product [data-reveal]').forEach((el) => observer.observe(el))
})
</script>

<template>
  <section id="about-product" class="product-showcase" aria-labelledby="about-product-title">
    <h2 id="about-product-title" class="visually-hidden">BuildLine platform showcase</h2>

    <div class="product-showcase__stack">
      <!-- Panel 1: Budget Dashboard (image left, text right) -->
      <article class="showcase-panel showcase-panel--thermal" data-reveal style="--reveal-delay: 0ms">
        <div class="showcase-panel__visual showcase-panel__visual--thermal" aria-hidden="true">
          <img
            class="showcase-shot showcase-shot--thermal"
            src="/assets/images/showcase/trimmed/dash1web.png"
            alt=""
            loading="lazy"
            decoding="async"
          >
        </div>

        <div class="showcase-panel__copy showcase-panel__copy--green">
          <h3 class="showcase-panel__title">
            <span>Visualize each budget deviation </span>
            <span class="showcase-panel__accent showcase-panel__accent--green">before</span>
            <span> it becomes a loss</span>
          </h3>

          <ul class="showcase-list">
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--green">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-thermal-wave.svg#icon"></use></svg>
              </span>
              <p>Control panels with configurable budget limits and automatic alerts for each purchase order.</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--green">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-thermal-bell.svg#icon"></use></svg>
              </span>
              <p>Immediate alerts when a materials order exceeds the budget allocated.</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--green">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-thermal-doc.svg#icon"></use></svg>
              </span>
              <p>Zero manual Excel spreadsheets, zero lost quotes on WhatsApp.</p>
            </li>
          </ul>

          <a href="#contact" class="btn showcase-panel__cta showcase-panel__cta--green">View dashboard</a>
        </div>
      </article>

      <!-- Panel 2: Alerts (text left, image right — reversed) -->
      <article class="showcase-panel showcase-panel--alerts showcase-panel--reverse" data-reveal style="--reveal-delay: 100ms">
        <div class="showcase-panel__copy showcase-panel__copy--red">
          <h3 class="showcase-panel__title">
            <span>Approvals that reach the right manager, at the </span>
            <span class="showcase-panel__accent showcase-panel__accent--red">right time,</span>
            <span> always</span>
          </h3>

          <ul class="showcase-list">
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--red">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-alert-warning.svg#icon"></use></svg>
              </span>
              <p>Alerts via WhatsApp and email when a budget overage or stock shortage occurs</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--red">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-alert-mail.svg#icon"></use></svg>
              </span>
              <p>Sent to the Logistics Manager or Project Manager, according to the configured approval workflow.</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--red">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-alert-chat.svg#icon"></use></svg>
              </span>
              <p>Real-time information to avoid emergency purchases and reduce logistical overcosts</p>
            </li>
          </ul>

          <a href="#contact" class="btn showcase-panel__cta showcase-panel__cta--red">View alerts</a>
        </div>

        <div class="showcase-panel__visual showcase-panel__visual--alerts" aria-hidden="true">
          <img
            class="showcase-shot showcase-shot--alerts"
            src="/assets/images/showcase/trimmed/dash2web.png"
            alt=""
            loading="lazy"
            decoding="async"
          >
        </div>
      </article>

      <!-- Panel 3: Cost History (image left, text right) -->
      <article class="showcase-panel showcase-panel--history" data-reveal style="--reveal-delay: 100ms">
        <div class="showcase-panel__visual showcase-panel__visual--history" aria-hidden="true">
          <img
            class="showcase-shot showcase-shot--history"
            src="/assets/images/showcase/trimmed/dash3web.png"
            alt=""
            loading="lazy"
            decoding="async"
          >
        </div>

        <div class="showcase-panel__copy showcase-panel__copy--orange">
          <h3 class="showcase-panel__title">
            <span class="showcase-panel__accent showcase-panel__accent--orange">Cost history</span>
            <span> and purchase traceability.</span>
          </h3>

          <ul class="showcase-list">
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--orange">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-history-database.svg#icon"></use></svg>
              </span>
              <p>Each order, quote, and invoice is saved by project.</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--orange">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-history-clipboard.svg#icon"></use></svg>
              </span>
              <p>Generates accounting-ready purchase order PDFs</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--orange">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-history-calendar.svg#icon"></use></svg>
              </span>
              <p>Real-time information for decision-making: Up-to-date data to negotiate better prices with suppliers.</p>
            </li>
          </ul>

          <a href="#contact" class="btn showcase-panel__cta showcase-panel__cta--orange">View reports</a>
        </div>
      </article>

      <!-- Panel 4: Multi-site (text left, image right — reversed) -->
      <article class="showcase-panel showcase-panel--sites showcase-panel--reverse" data-reveal style="--reveal-delay: 100ms">
        <div class="showcase-panel__copy showcase-panel__copy--blue">
          <h3 class="showcase-panel__title">
            <span>Complete control of your projects and supplies in </span>
            <span class="showcase-panel__accent showcase-panel__accent--blue">one place</span>
            <span>.</span>
          </h3>

          <ul class="showcase-list">
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--blue">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-sites-map.svg#icon"></use></svg>
              </span>
              <p>Monitor the status of each order from the moment the request is made.</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--blue">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-sites-bars.svg#icon"></use></svg>
              </span>
              <p>Detects budget deviations before they occur.</p>
            </li>
            <li class="showcase-list__item">
              <span class="showcase-list__icon showcase-list__icon--blue">
                <svg viewBox="0 0 24 24" aria-hidden="true"><use href="/assets/icons/showcase-sites-star.svg#icon"></use></svg>
              </span>
              <p>Prioritize critical purchases to avoid work stoppages.</p>
            </li>
          </ul>

          <a href="#contact" class="btn showcase-panel__cta showcase-panel__cta--blue">View multi-site</a>
        </div>

        <div class="showcase-panel__visual showcase-panel__visual--sites" aria-hidden="true">
          <img
            class="showcase-shot showcase-shot--sites"
            src="/assets/images/showcase/trimmed/dash4web.png"
            alt=""
            loading="lazy"
            decoding="async"
          >
        </div>
      </article>
    </div>
  </section>
</template>

<style scoped>
/* Scoped styles are intentionally left empty since global styles handle the layout. */
</style>
