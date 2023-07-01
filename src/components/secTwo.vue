<template>
  <div class="bg">
    <div class="container text-center mt-5">
      <div class="title text-center">
        <h1 class="" data-aos="fade-up" data-aos-duration="1000">
          Lorem ipsum dolor sit amet.
        </h1>
        <p class="" data-aos="fade-up" data-aos-duration="2000">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. In
          recusandae dolor, omnis unde voluptas aliquam.
        </p>
      </div>
      <div class="row g-3">
        <div
          class="col-xxl-3 col-lg-3 col-md-6 mm mt-5"
          v-for="image in images"
          :key="image.id"
        >
          <div class="circle" data-aos="fade-up" data-aos-duration="3000">
            <div class="content">
              <img :src="image.path" alt="" />
              <div class="circle-text">{{ image.text }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  data() {
    return {
      images: [
        { id: 1, path: require("@/assets/c1.png"), text: "one" },
        { id: 2, path: require("@/assets/c2.png"), text: "two" },
        { id: 3, path: require("@/assets/cs.png"), text: "three" },
        { id: 4, path: require("@/assets/c4.png"), text: "four" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  color: #555;
}
.bg {
  background: url(@/assets/Layer-6.png);
  width: 100%;
  height: 100vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
@media (max-width: 1200px) {
  .mm {
    flex-basis: 50%;
    max-width: 50%;
    padding-top: 40px;
    position: relative;
    top: -70px;
  }
  .container {
    position: relative;
    top: 100px;
  }
  .circle img {
    width: 200px;
  }
}
@media (max-width: 500px) {
  .circle {
    position: relative;
    top: 100px;
  }
  .circle img {
    width: 150px;
  }
}

.mm {
}
.circle {
  position: relative;
  .circle-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
    font-size: 2rem;
    text-shadow: 4px 5px 5px black;
    text-transform: capitalize;
  }
}
.circle {
  .content {
    position: relative;
  }
}
@media screen and (min-width: 1400px) {
  .content {
    margin-top: 130px;
  }
}
.title {
  position: relative;
  top: 20px;
}
</style>
