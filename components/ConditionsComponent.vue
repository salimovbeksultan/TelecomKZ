<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="conditions-wrapper">
    <div class="conditions-title">{{ t('conditions_title') }}</div>
    <div class="conditions-row">
      <div class="conditions-item"><span v-html="t('conditions.0')"></span></div>
      <div class="conditions-item"><span v-html="t('conditions.1')"></span></div>
      <div class="conditions-item"><span v-html="t('conditions.2')"></span></div>
      <div class="conditions-item"><span v-html="t('conditions.3')"></span></div>
    </div>
  </section>
</template>

<style scoped>
.conditions-wrapper {
  padding-top: 4vw;
  padding-bottom: 5vw;
  background-image: url('../assets/snow.png');
  background-color: rgba(220, 230, 255, 1);
}

.conditions-title {
  color: rgba(23, 54, 183, 1);
  text-align: center;
  font-family: 'Helvetica Neue';
  font-weight: 700;
  font-size: 5vw;
  text-transform: uppercase;
}

.conditions-row {
  display: flex;
  width: 100%;
  gap: 0.8vw;
  align-items: center;
  justify-content: center;
  padding-top: 3.6vw;
}

.conditions-item {
  border-radius: 2.6vw;
  padding-left: 3.2vw;
  padding-right: 3.2vw;
  padding-top: 3.4vw;
  padding-bottom: 3.4vw;
  font-family: 'Helvetica Neue';
  font-size: 1.9vw;
  background-color: rgba(64, 95, 239, 1);
  width: 16vw;
  color: rgba(255, 255, 255, 1);
  height: 16vw;
  z-index: 2;
}

.conditions-item:nth-child(even) {
  background-color: rgba(255, 255, 255, 1);
  color: rgba(23, 54, 183, 1);
}

@media (max-width: 640px) {
  .conditions-title {
    font-size: 8.5vw;
  }

  .conditions-row {
    flex-direction: column;
    gap: 3vw;
  }

  .conditions-item {
    width: 71vw;
    height: 30vw;
    font-size: 5vw;
    padding: 6vw;
    border-radius: 5.3vw;
    display: flex;
    align-items: center;
  }
}
</style>
