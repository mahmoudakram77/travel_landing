<template>
  <div class="container-fluid mt-5 text-center" v-if="false">
    <h1 class="mt-5 mb-5" data-aos="fade-up" data-aos-duration="1000">
      Lorem ipsum dolor sit.
    </h1>

    <div class="row mt-5">
      <div
        class="col-xxl-4 col-md-6 position-relative"
        v-for="img in images"
        :key="img.id"
      >
        <div class="img-container" data-aos="fade-up" data-aos-duration="1500">
          <img :src="img.path" alt="" />

          <div class="img-text">
            <h1>{{ img.text }}</h1>
            <h3>{{ img.para }}</h3>
            <button>{{ img.btn }}</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          id: 1,
          path: require("@/assets/5.png"),
          text: "TITLE",
          para: "discription",
          btn: "KNOW MORE",
        },
        {
          id: 2,
          path: require("@/assets/6.png"),
          text: "TITLE",
          para: "description",
          btn: "KNOW MORE",
        },
        {
          id: 3,
          path: require("@/assets/7.png"),
          text: "TITLE",
          para: "description",
          btn: "KNOW MORE",
        },
        {
          id: 4,
          path: require("@/assets/8.png"),
          text: "TITLE",
          para: "description",
          btn: "KNOW MORE",
        },
        {
          id: 5,
          path: require("@/assets/9.png"),
          text: "TITLE",
          para: "description",
          btn: "KNOW MORE",
        },
        {
          id: 6,
          path: require("@/assets/4.png"),
          text: "TITLE",
          para: "description",
          btn: "KNOW MORE",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
* {
  overflow-x: hidden;
}
* {
  overflow: hidden;
}
.container {
  overflow-x: hidden;
}
img {
  width: 480px;
  margin-top: 10px;
  height: 400px;
  margin-bottom: 10px;
  padding: 20px;
}

.img-container {
  position: relative;
}

.img-container:hover .img-text {
  opacity: 1 !important;
}

.img-text {
  position: absolute;
  z-index: 999;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  color: white;
  transition: 1s ease all;
}

button {
  background: blue;
  border: none;
  color: white;
  padding: 10px;
  border-radius: 10px;
}

.img-text,
h1 {
  text-transform: uppercase;
}

img {
}
.padding-0 {
  padding-right: 0;
  padding-left: 0;
}
@media screen and (max-width: 768px) {
  img {
    width: 420px;
    height: 380px;
  }
  .img-container {
    display: flex;
    justify-content: center;
  }
}
</style>
