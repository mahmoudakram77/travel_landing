<template>
  <transition name="fade">
    <div class="top" v-show="show" @click="scrollToTop">
      <i class="fa-sharp fa-regular fa-circle-up"></i>
    </div>
  </transition>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      windowHight: 0,
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
    showButton() {
      this.windowHight = window.scrollY;
      if (this.windowHight >= 300) {
        this.show = true;
      } else {
        this.show = false;
      }
    },
  },
  mounted() {
    window.addEventListener("scroll", this.showButton);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.showButton);
  },
};
</script>

<style lang="scss" scoped>
* {
  overflow-x: hidden;
}
.top {
  position: fixed;
  bottom: 15px;
  right: 10px;
  i {
    font-size: 40px;
    cursor: pointer;
    color: white;
    background: linear-gradient(
      50deg,
      rgba(1, 0, 11, 1) 0%,
      rgba(20, 149, 235, 1) 100%,
      rgba(0, 0, 0, 1) 100%
    );

    transition: 1s ease all;
    border-radius: 20px;
    border: 2px solid rgba(20, 149, 235, 1);
    &:hover {
      transition: 1s ease all;
    }
  }
  &.fade-enter-active,
  &.fade-leave-active {
    transition: opacity 0.5s ease;
  }
  &.fade-enter-from {
    opacity: 0;
    animation: anmie 1s infinite;
  }
  &.fade-enter-to {
    opacity: 1;
    animation: anmie 1s infinite;
  }
  &.fade-leave-to {
    opacity: 0;
    animation: anmiereverse 1s;
  }
}
@keyframes anmie {
  0% {
    transform: scale(0);
  }
  100% {
  }
}
@keyframes anmiereverse {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(0);
  }
}
.top {
  animation: upup 1s infinite alternate-reverse;
  &:hover {
    animation-play-state: paused;
  }
}
@keyframes upup {
  0% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0px);
  }
}
</style>
