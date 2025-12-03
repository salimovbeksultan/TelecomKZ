<script setup>
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="prizes-wrapper">
    <div class="prizes-title" v-html="t('prizes_title')"></div>
    <div class="prizes-first-row" style="padding-top: 4vw">
      <div class="prizes-item">
        <img class="prizes-item-circle" alt="ipad" src="../assets/ipad.png" />
        <div class="prizes-item-box">
          <div class="prize-place">{{ t('prizes.0.place') }}</div>
          <div class="prize-name">{{ t('prizes.0.prize') }}</div>
        </div>
      </div>
      <div class="prizes-item">
        <img class="prizes-item-circle" alt="ipad" src="../assets/earpods.png" />
        <div class="prizes-item-box">
          <div class="prize-place">{{ t('prizes.1.place') }}</div>
          <div class="prize-name">{{ t('prizes.1.prize') }}</div>
        </div>
      </div>
    </div>
    <div class="prizes-first-row" style="padding-top: 3vw">
      <div class="prizes-sub-item">
        <img class="prizes-item-sub-circle" alt="ipad" src="../assets/15000-bonus.png" />
        <div class="prizes-item-sub-box">
          <div class="prize-sub-place">{{ t('prizes.2.place') }}</div>
          <div class="prize-sub-name">{{ t('prizes.2.prize') }}</div>
        </div>
      </div>
      <div class="prizes-sub-item">
        <img class="prizes-item-sub-circle" alt="ipad" src="../assets/10000-bonus.png" />
        <div class="prizes-item-sub-box">
          <div class="prize-sub-place">{{ t('prizes.3.place') }}</div>
          <div class="prize-sub-name">{{ t('prizes.3.prize') }}</div>
        </div>
      </div>
      <div class="prizes-sub-item">
        <img class="prizes-item-sub-circle" alt="ipad" src="../assets/1000-bonus.png" />
        <div class="prizes-item-sub-box">
          <div class="prize-sub-place">{{ t('prizes.4.place') }}</div>
          <div class="prize-sub-name">{{ t('prizes.4.prize') }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.prizes-wrapper {
  background-color: rgba(220, 230, 255, 1);
  padding-top: 5vw;
  padding-bottom: 5vw;
}

.prizes-title {
  color: rgba(23, 54, 183, 1);
  font-weight: 700;
  font-family: 'Helvetica Neue';
  font-size: 5vw;
  text-transform: uppercase;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
}

.prizes-first-row {
  width: 100%;
  display: flex;
  gap: 9vw;
  justify-content: center;
}

.prizes-item {
  display: flex;
  flex-direction: column;
  width: 32vw;
  align-items: center;
}

.prizes-sub-item {
  display: flex;
  flex-direction: column;
  width: 24vw;
  align-items: center;
}

.prizes-item-circle {
  height: 24vw;
  width: 24vw;
  position: relative;
  z-index: 2;
  margin-bottom: -16vw;
}

.prizes-item-sub-circle {
  height: 18vw;
  width: 18vw;
  position: relative;
  z-index: 2;
  margin-bottom: -12vw;
}

.prizes-item-box {
  width: 32vw;
  height: 26vw;
  background: linear-gradient(163.11deg, #7aa7f9 5.5%, #577cf3 68.06%, #2e48eb 118.25%);
  border-radius: 3vw;

  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding-bottom: 2vw;

  position: relative;
  z-index: 1;
}

.prizes-item-sub-box {
  width: 24vw;
  height: 19vw;
  background: linear-gradient(163.11deg, #7aa7f9 5.5%, #577cf3 68.06%, #2e48eb 118.25%);
  border-radius: 3vw;

  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding-bottom: 2vw;

  position: relative;
  z-index: 1;
}

.prize-place {
  color: rgba(255, 255, 255, 1);
  font-weight: 700;
  font-family: 'Helvetica Neue';
  font-size: 4.5vw;
  letter-spacing: -0.02em;
}

.prize-sub-place {
  color: rgba(255, 255, 255, 1);
  font-weight: 700;
  font-family: 'Helvetica Neue';
  font-size: 3.3vw;
  letter-spacing: -0.02em;
}

.prize-name {
  color: rgba(255, 255, 255, 1);
  font-weight: 400;
  font-style: normal;
  font-family: 'Helvetica Neue';
  font-size: 3.5vw;
  letter-spacing: -0.02em;
}

.prize-sub-name {
  color: rgba(255, 255, 255, 1);
  font-weight: 400;
  font-style: normal;
  font-family: 'Helvetica Neue';
  font-size: 2.5vw;
  letter-spacing: -0.02em;
}

@media (max-width: 640px) {
  .prizes-title {
    font-size: 8.5vw;
    width: 80vw;
  }

  .prizes-first-row {
    flex-direction: column;
    align-items: center;
  }

  .prizes-item {
    width: 69vw;
  }

  .prizes-item-circle {
    width: 50vw;
    height: 50vw;
    margin-bottom: -22vw;
  }

  .prizes-item-box {
    width: 60vw;
    height: 40vw;
  }

  .prize-place {
    font-size: 9vw;
  }

  .prize-name {
    font-size: 7vw;
  }

  .prize-sub-place {
    font-size: 9vw;
  }

  .prize-sub-name {
    font-size: 7vw;
  }

  .prizes-sub-item {
    width: 69vw;
  }

  .prizes-item-sub-circle {
    width: 50vw;
    height: 50vw;
    margin-bottom: -22vw;
  }

  .prizes-item-sub-box {
    width: 60vw;
    height: 40vw;
  }
}
</style>
