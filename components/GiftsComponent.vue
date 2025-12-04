<script setup></script>

<template>
  <img class="icon first-gift" alt="gift" src="../assets/gift.png" />
  <img class="icon second-gift" alt="gift" src="../assets/accessory.png" />
  <img class="icon third-gift" alt="gift" src="../assets/gift-reversed.png" />
  <img class="icon fourth-gift" alt="gift" src="../assets/accessory-reversed.png" />
  <img class="icon fifth-gift" alt="gift" src="../assets/gift-reversed.png" />
  <img class="icon sixth-gift" alt="gift" src="../assets/gift.png" />
  <img class="icon seventh-gift" alt="gift" src="../assets/accessory.png" />
  <img class="icon eighth-gift" alt="gift" src="../assets/gift-reversed.png" />
  <img class="icon ninth-gift" alt="gift" src="../assets/accessory.png" />
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

.sixth-gift {
  display: none;
}

.seventh-gift {
  display: none;
}

.eighth-gift {
  top: 193vw;
  z-index: 2;
  right: -5vw;
  height: 16vw;
  width: 16vw;
}

.ninth-gift {
  top: 220vw;
  z-index: 2;
  left: 0vw;
  height: 7vw;
  width: 7vw;
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
    top: 300vw;
    height: 35.2vw;
    width: 35.2vw;
    left: -15vw;
  }

  .fourth-gift {
    top: 420vw;
    height: 28vw;
    width: 28vw;
    left: -10vw;
  }

  .fifth-gift {
    display: block;
    top: 220vw;
    height: 16vw;
    width: 16vw;
    right: -6vw;
  }

  .sixth-gift {
    display: block;
    height: 31vw;
    width: 31vw;
    right: -10vw;
    top: 450vw;
  }

  .seventh-gift {
    display: block;
    height: 16vw;
    width: 16vw;
    right: -5vw;
    top: 355vw;
  }

  .eighth-gift {
    display: block;
    z-index: 0;
    width: 39vw;
    height: 39vw;
    top: 780vw;
    right: -10vw;
  }

  .ninth-gift {
    display: block;
    z-index: 0;
    width: 31.2vw;
    height: 31.2vw;
    top: 910vw;
    left: -10vw;
  }
}
</style>
