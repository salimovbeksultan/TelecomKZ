<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="download-wrapper">
    <div class="download-row">
      <div>
        <div
          class="download-text"
          :class="t('downloads.0.size')"
          v-html="t('downloads.0.text')"
        ></div>
        <div
          class="download-text"
          :class="t('downloads.1.size')"
          v-html="t('downloads.1.text')"
        ></div>
        <div
          class="download-text"
          :class="t('downloads.2.size')"
          v-html="t('downloads.2.text')"
        ></div>
        <div class="download-buttons">
          <a href="https://apps.apple.com/us/app/telecom-kz/id1545816005"
            ><img class="download-button" alt="app-store" src="../assets/app-store.png" />
          </a>
          <a href="https://play.google.com/store/apps/details?id=kz.telecom.app"
            ><img class="download-button" alt="google-play" src="../assets/google-play.png"
          /></a>
        </div>
      </div>
      <img class="download-qr" src="../assets/qr.png" alt="qr" />
      <img class="download-qr-mobile" src="../assets/qr-mobile.png" alt="qr" />
    </div>
  </section>
</template>

<style>
.download-wrapper {
  background: radial-gradient(
    60.53% 301.18% at 91.51% 44.85%,
    #77a4f9 0%,
    #5d82f4 41.54%,
    #4060ef 100%
  );
  padding-top: 3vw;
}

.download-row {
  display: flex;
  padding-left: 5vw;
}

.download-text {
  color: rgba(255, 255, 255, 1);
  font-family: 'Helvetica Neue';
}

.download-buttons {
  padding-top: 2vw;
  gap: 2.6vw;
  display: flex;
}

.download-button {
  width: 20vw;
  height: 7vw;
}

.download-qr {
  width: 50vw;
  margin-left: -3vw;
}

.text-big {
  font-size: 9vw;
}

.text-medium {
  font-size: 3vw;
}

.download-qr-mobile {
  display: none;
}

@media (max-width: 640px) {
  .download-wrapper {
    padding-top: 8vw;
  }

  .download-row {
    flex-direction: column;
    padding-left: 0;
    align-items: center;
  }

  .download-text {
    text-align: center;
  }

  .download-buttons {
    gap: 5vw;
    padding-bottom: 12vw;
  }

  .download-button {
    width: 36vw;
    height: 12.5vw;
  }

  .download-qr {
    display: none;
  }

  .download-qr-mobile {
    display: block;
    width: 100%;
  }

  .text-medium {
    font-size: 5vw;
  }

  .text-big {
    font-size: 13vw;
  }
}
</style>
