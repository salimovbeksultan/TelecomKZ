<script setup></script>

<template>
  <img class="icon first-gift" alt="gift" src="../assets/gift.png" />
  <img class="icon second-gift" alt="gift" src="../assets/accessory.png" />
  <img class="icon third-gift" alt="gift" src="../assets/gift-reversed.png" />
  <img class="icon fourth-gift" alt="gift" src="../assets/accessory-reversed.png" />
  <img class="icon fifth-gift" alt="gift" src="../assets/gift-reversed.png" />

</template>

<style scoped>
.icon {
  font-size: 3.75rem;
  transition: transform 0.4s ease;
  z-index: 2;
  position: absolute;
  animation: float 6s ease-in-out infinite;
}

.first-gift {
  height: 16vw;
  width: 16vw;
  right: 0;
  top: 65vw;
}

.second-gift {
  height: 16vw;
  width: 16vw;
  left: -2vw;
  top: 65vw;
}

.third-gift {
  height: 12vw;
  width: 12vw;
  left: 0;
  top: 94vw;
}

.fourth-gift {
  height: 10vw;
  width: 10vw;
  right: 0;
  top: 100vw;
}

.fifth-gift {
  display: none;
}

.icon:hover {
  transform: scale(1.2) rotate(15deg);
}
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-15px);
  }
  100% {
    transform: translateY(0px);
  }
}

@media (max-width: 640px) {
  .first-gift {
    top: 115vw;
    height: 35vw;
    width: 35vw;
    right: -14vw;
  }

  .second-gift {
    top: 150vw;
    height: 40vw;
    width: 40vw;
    left: -15vw;
  }

  .third-gift {
    top: 400vw;
    height: 30vw;
    width: 30vw;
    left: -5vw;
  }

  .fourth-gift {
    top: 480vw;
    height: 28vw;
    width: 28vw;
  }

  .fifth-gift {
    display: block;
    top: 220vw;
    height: 16vw;
    width: 16vw;
    right: -6vw;
  }
}
</style>
