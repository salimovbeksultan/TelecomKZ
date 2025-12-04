<script setup>
import { useI18n } from 'vue-i18n'

const { t, locale } = useI18n()

function switchLanguage() {
  if (locale.value === 'ru') locale.value = 'kz'
  else locale.value = 'ru'
}
</script>

<template>
  <section class="header-wrapper">
    <div class="header-content">
      <div class="first-row">
        <img src="../assets/logo.svg" class="logo-image" alt="Logo"></img>
        <div @click="switchLanguage" class="language-switcher">
            <img src="../assets/lang.svg" class="language-icon" alt="lang-switcher"></img>
            <span class="language-text">{{ t('other_language') }}</span>
        </div>
      </div>
      <div class="first-row mobile-row" style="padding-top: 1vw;">
        <div class="header-text-col">
            <div class="header-text-secondary" :class="t('header.0.size')">{{ t('header.0.value') }}</div>
            <div class="header-text-secondary" :class="t('header.1.size')">{{ t('header.1.value') }}</div>
            <div class="header-text-secondary" :class="t('header.2.size')">{{ t('header.2.value') }}</div>
            <div class="header-text-secondary" :class="t('header.3.size')">{{ t('header.3.value') }}</div>
            <a style="text-decoration: none;" href="https://telecom.kz/ru/customer/auth/login"><div class="header-button">{{ t("download") }}</div></a>
        </div>
        <img src="../assets/gifts.png" alt="gifts" class="gifts-image" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.header-wrapper {
  width: 100%;
  height: 50vw;
  background: radial-gradient(
    90.16% 360.62% at 9.84% 44.06%,
    #1529e7 0%,
    #4869f0 54.57%,
    #7dacfa 100%
  );
}

.header-content {
  padding-top: 4vw;
  padding-left: 4vw;
  padding-right: 4vw;
}

.first-row {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo-image {
    width: 15vw;
}

.language-switcher {
    background: rgba(255, 255, 255, 1);
    border-radius: 1vw;
    height: 1.3vw;
    padding-top: 0.3vw;
    padding-bottom: 0.3vw;
    width: 4vw;
    padding-left: 0.6vw;
    padding-right: 0.6vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.language-switcher:hover {
    cursor: pointer;
}

.language-text {
    font-family: 'Helvetica Neue';
    font-weight: 500;
    font-style: normal;
    font-size: 1.2vw;
    line-height: 110.00000000000001%;
    color: rgba(23, 54, 183, 1);
}

.language-icon {
    height: 1.35vw;
    width: 1.35vw;
}

.gifts-image {
    width: 42vw;
    height: 38vw;
    margin-left: -7vw;
}

.header-text-col {
    display: flex;
    flex-direction: column;
}

.header-text-secondary {
    font-family: 'Helvetica Neue';
    font-weight: 700;
    font-style: bold;
    line-height: 110.00000000000001%;
    color: rgba(255, 255, 255, 1);
    letter-spacing: -0.02em;
}

.header-button {
    text-transform: uppercase;
    font-family: 'Helvetica Neue';
    font-weight: 700;
    padding-left: 7vw;
    padding-right: 7vw;
    padding-top: 2vw;
    padding-bottom: 2vw;
    background-color: rgba(255, 237, 76, 1);
    color: rgba(23, 54, 183, 1);
    font-size: 3.5vw;
    border-radius: 3vw;
    width: 17vw;
    text-align: center;
    margin-top: 5vw;
}

.header-button:hover {
    cursor: pointer;
}

@media (max-width: 640px) {
  .logo-image {
    width: 36vw;
  }

  .header-wrapper {
    height: 88vw;
  }

  .gifts-image {
    margin-left: 0;
    height: 52vw;
    width: 57.8vw;
    top: 32vw;
    right: 0;
    position: absolute;
  }


  .language-switcher {
    width: 13vw;
    height: 6.6vw;
    border-radius: 3.2vw;
    padding-left: 1.8vw;
    padding-right: 1.8vw;
  }

  .language-icon {
    height: 4.2vw;
    width: 4.2vw;
  }

  .language-text {
    font-size: 3.7vw;
  }

  .mobile-row {
    flex-direction: column;
  }

  .header-text-col {
    margin-left: -28vw;
  }

  .header-button {
    width: 25vw;
    border-radius: 3.2vw;
    font-size: 5.3vw;
    padding-right: 6vw;
    padding-left: 6vw;
    top: 65vw;
    position: absolute;
    padding-top: 2.4vw;
    padding-bottom: 2.4vw;
  }
}
</style>
