<template>
  <div class="search hello">
    <i
      style="color: white"
      @click="showing"
      class="d- fa-solid fa-magnifying-glass"
    ></i>
  </div>
  <transition name="modal">
    <div class="modal-mask" v-if="show">
      <div class="modal-weapper">
        <div class="modal-container">
          <div class="modal-footer position-relative">
            <div class="closee" @click="notShow">
              <i class="fa-solid fa-xmark"></i>
            </div>
            <div class="d-flex">
              <input type="search" />
              <button class="modal-default-button close sear">Search</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  data() {
    return {
      show: null,
    };
  },
  methods: {
    showing() {
      this.show = true;
    },
    notShow() {
      this.show = false;
    },
  },
};
</script>

<style lang="scss" scoped>
* {
}
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-container {
  background-color: rgb(255, 244, 244);
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border-radius: 2px;
  transition: all 0.3s ease;
  width: 330px;
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the modal transition by editing
 * these styles.
 */

.modal-enter-from,
.modal-leave-to {
  opacity: 0;
}

.modal-enter-active .modal-container {
  transition: 1s ease all;
}
.modal-leave-active .modal-container {
  transition: 1s ease all;
}
.modal-enter-from {
  animation: anmi 0.2s;
}
.modal-enter-to {
  animation: anmi 0.2s;
}
.modal-leave-to {
  animation: anmi2 0.3s;
}

@keyframes anmi {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes anmi2 {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  100% {
    transform: scale(0);
    opacity: 0;
  }
}
.search {
  position: absolute;
  top: -4px;
  right: 15px;
  cursor: pointer;
  z-index: 9999;
  font-size: 25px;
}
.closee {
  position: absolute;
  top: -35px;
  right: -35px;
  cursor: pointer;
  transition: 1s ease all;
  font-size: 30px;
  &:hover {
    color: black;
    transition: 0.5 ease all;
    transform: rotate(90deg) scale(1.3);
  }
}
@media screen and (max-width: 650px) {
  input {
    width: 140px;
    flex-direction: row;
  }
}
@media screen and (max-width: 330px) {
  input {
    width: 90px;
    flex-direction: row;
  }
}
.sear {
  background: blue;

  border: 1px solid blue;
  color: white;
  text-shadow: 0 0 10px black;
  border-radius: 0 10px 10px 0;
  transition: 1s ease all;
  &:hover {
    background: rgba(37, 37, 255, 0.858);
    border: 1px solid rgba(37, 37, 255, 0.858);
  }
}
input {
  border-radius: 10px 0 0 10px;
  padding: 5px;
  box-shadow: 0 0 1px rgb(240, 240, 240);
  color: blue;
  outline: none;
}
@media screen and (max-width: 500px) {
  .modal-container {
    width: 270px;
  }
}
</style>
