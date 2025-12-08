<script setup>
import { useI18n } from 'vue-i18n'

const { t, locale } = useI18n()

const getImgUrl = (imageName) => {
  return new URL(`../assets/${imageName}`, import.meta.url).href
}
</script>

<template>
  <section class="rules-wrapper">
    <div class="trees-container">
      <img src="@/assets/eve.png" alt="eve" class="decor-branch branch-left" />
      <img src="@/assets/eve-1.png" alt="eve" class="decor-branch branch-center" />
      <img src="@/assets/eve-2.png" alt="eve" class="decor-branch branch-right" />
      <img src="@/assets/eve-mobile.png" alt="eve" class="decor-branch branch-mobile" />
    </div>

    <div class="content-container">
      <h2 class="section-title">{{ t('rules_title') }}</h2>

      <div class="cards-wrapper">
        <div class="card">
          <img v-if="locale === 'ru'" class="card-image" src="@/assets/card-1.png" alt="card-1" />
          <img v-else class="card-image" src="@/assets/card-1-kz.png" alt="card-1" />
          <div class="card-text">
            <div class="card-title" v-html="t('rules_cards.0.title')"></div>
            <div class="card-subtitle" v-html="t('rules_cards.0.subtitle')"></div>
          </div>
        </div>
        <div class="card">
          <img class="card-image" src="@/assets/card-2.png" alt="card-1" />
          <div class="card-text">
            <div class="card-title" v-html="t('rules_cards.1.title')"></div>
            <div class="card-subtitle" v-html="t('rules_cards.1.subtitle')"></div>
          </div>
        </div>
        <div class="card">
          <img class="card-image" src="@/assets/card-3.png" alt="card-1" />
          <div class="card-text">
            <div class="card-title" v-html="t('rules_cards.2.title')"></div>
            <div class="card-subtitle" v-html="t('rules_cards.2.subtitle')"></div>
          </div>
        </div>
        <div class="card">
          <img class="card-image" src="@/assets/card-4.png" alt="card-1" />
          <div class="card-text">
            <div class="card-title" v-html="t('rules_cards.3.title')"></div>
            <div class="card-subtitle" v-html="t('rules_cards.3.subtitle')"></div>
          </div>
        </div>
        <div class="card">
          <img v-if="locale === 'ru'" class="card-image" src="@/assets/card-5.png" alt="card-1" />
          <img v-else class="card-image" src="@/assets/card-5-kz.png" alt="card-1" />
          <div class="card-text">
            <div class="card-title" v-html="t('rules_cards.4.title')"></div>
            <div class="card-subtitle" v-html="t('rules_cards.4.subtitle')"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.rules-wrapper {
  background: linear-gradient(247.54deg, #77a4f9 3.61%, #486af0 59.25%, #3551ed 107.4%);
  width: 100%;
  padding-top: 4vw;
  overflow: hidden;
  position: relative;
}

.trees-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: 1;
}

.decor-branch {
  position: absolute;
  bottom: 0;
  width: 25vw;
}

.branch-left {
  left: 0px;
  bottom: 0px;
}

.branch-right {
  right: 0px;
  bottom: 0px;
}

.branch-center {
  left: 0;
  bottom: 0px;
  opacity: 0.8;
}

.content-container {
  position: relative;
  z-index: 2;
  max-width: 100%;
  margin: 0 auto;
}

.section-title {
  color: rgba(255, 255, 255, 1);
  text-transform: uppercase;
  font-size: 4vw;
  margin-bottom: 3vw;
  font-weight: 700;
  font-family: 'Helvetica Neue';
  text-align: center;
}

.cards-wrapper {
  display: flex;
  padding-bottom: 6.7vw;
  justify-content: center;
}

.card {
  box-shadow: -14px 9px 30px 0px rgba(88, 86, 86, 0.25);
  background-color: rgba(255, 255, 255, 1);
  border-radius: 2.6vw;
  display: flex;
  flex-direction: column;
  width: 16vw;
  padding-left: 1vw;
  padding-right: 1vw;
  margin-left: -0.5vw;
}

.card:first-child {
  margin-left: 0;
}

.card-image {
  width: 16vw;
  height: 16vw;
  object-fit: cover;
}

.card-text {
  padding-bottom: 4vw;
  font-family: 'Helvetica Neue';
}

.card-title {
  color: rgba(23, 54, 183, 1);
  font-weight: 700;
  font-size: 2vw;
  line-height: 96%;
}

.card-subtitle {
  padding-top: 8px;
  color: rgba(58, 86, 213, 1);
  font-weight: 400;
  font-size: 1vw;
}

.branch-mobile {
  display: none;
}

@media (max-width: 640px) {
  .section-title {
    font-size: 8vw;
    width: 50vw;
    margin-left: auto;
    margin-right: auto;
    margin-top: 0;
  }

  .cards-wrapper {
    flex-direction: column;
    align-items: center;
    gap: 2.6vw;
  }

  .card {
    margin-left: 0;
    width: 74vw;
    padding-left: 5vw;
    flex-direction: row;
    height: 38vw;
    justify-content: space-around;
  }

  .card-title {
    font-size: 5vw;
  }

  .card-subtitle {
    font-size: 3.7vw;
  }

  .card-text {
    padding-top: 5vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .card-image {
    order: 2;
    width: 34vw;
    height: 34vw;
    top: 0;
  }

  .branch-mobile {
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    width: 32vw;
  }
}
</style>
