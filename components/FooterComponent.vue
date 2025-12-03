<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="footer-wrapper">
    <div class="footer-content">{{ t('footer') }}</div>
  </section>
</template>

<style>
.footer-wrapper {
  background-color: rgba(220, 230, 255, 1);
  width: 100%;
  padding-top: 3vw;
  padding-bottom: 2.8vw;
}

.footer-content {
  padding-left: 5vw;
  padding-right: 5vw;
  font-size: 0.8vw;
  font-weight: 400;
  font-family: 'Helvetica Neue';
  color: rgba(128, 131, 149, 1);
}

@media (max-width: 640px) {
  .footer-content {
    font-size: 1.8vw;
    padding-bottom: 9vw;
  }
}
</style>
