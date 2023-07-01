<template>
  <h1
    class="text-center h1"
    data-aos="zoom-in"
    data-aos-easing="linear"
    data-aos-duration="1500"
  >
    Lorem ipsum dolor sit amet consectetur
  </h1>
  <Splide class="container" :options="options" aria-label="My Favorite Images">
    <SplideSlide class="container">
      <div class="cardd">
        <img src="@/assets/5.png" alt="Sample 1" />
        <h1>Lorem, ipsum.</h1>
        <div class="new d-flex justify-content-between">
          <div class="d-flex">
            <i class="mt-1 mx-2 fa-solid fa-user-secret"></i>
            <p class="">ADMIN</p>
          </div>
          <div class="d-flex">
            <i class="mt-1 fa-solid fa-calendar-days"></i>
            <p class="mx-2">May,11-2023</p>
          </div>
        </div>

        <p class="para">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet,
          animi Lorem ipsum dolor sit, amet consectetur adipisicing elit.
          Eveniet, animi.
        </p>
      </div>
    </SplideSlide>
    <SplideSlide class="container mx-auto">
      <div class="cardd">
        <img src="@/assets/6.png" alt="Sample 1" />
        <h1>Lorem, ipsum.</h1>
        <div class="new d-flex justify-content-between">
          <div class="d-flex">
            <i class="mt-1 mx-2 fa-solid fa-user-secret"></i>
            <p class="">ADMIN</p>
          </div>
          <div class="d-flex">
            <i class="mt-1 fa-solid fa-calendar-days"></i>
            <p class="mx-2">May,11-2023</p>
          </div>
        </div>

        <p class="para">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet,
          animi Lorem ipsum dolor sit, amet consectetur adipisicing elit.
          Eveniet, animi.
        </p>
      </div>
    </SplideSlide>
    <SplideSlide class="container mx-auto">
      <div class="cardd">
        <img src="@/assets/7.png" alt="Sample 1" />
        <h1>Lorem, ipsum.</h1>
        <div class="new d-flex justify-content-between">
          <div class="d-flex">
            <i class="mt-1 mx-2 fa-solid fa-user-secret"></i>
            <p class="">ADMIN</p>
          </div>
          <div class="d-flex">
            <i class="mt-1 fa-solid fa-calendar-days"></i>
            <p class="mx-2">May,11-2023</p>
          </div>
        </div>

        <p class="para">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet,
          animi Lorem ipsum dolor sit, amet consectetur adipisicing elit.
          Eveniet, animi.
        </p>
      </div>
    </SplideSlide>
    <SplideSlide class="container mx-auto">
      <div class="cardd">
        <img src="@/assets/8.png" alt="Sample 1" />
        <h1>Lorem, ipsum.</h1>
        <div class="new d-flex justify-content-between">
          <div class="d-flex">
            <i class="mt-1 mx-2 fa-solid fa-user-secret"></i>
            <p class="">ADMIN</p>
          </div>
          <div class="d-flex">
            <i class="mt-1 fa-solid fa-calendar-days"></i>
            <p class="mx-2">May,11-2023</p>
          </div>
        </div>

        <p class="para">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet,
          animi Lorem ipsum dolor sit, amet consectetur adipisicing elit.
          Eveniet, animi.
        </p>
      </div>
    </SplideSlide>
    <SplideSlide class="container mx-auto">
      <div class="cardd">
        <img src="@/assets/6.png" alt="Sample 1" />
        <h1>Lorem, ipsum.</h1>
        <div class="new d-flex justify-content-between">
          <div class="d-flex">
            <i class="mt-1 mx-2 fa-solid fa-user-secret"></i>
            <p class="">ADMIN</p>
          </div>
          <div class="d-flex">
            <i class="mt-1 fa-solid fa-calendar-days"></i>
            <p class="mx-2">May,11-2023</p>
          </div>
        </div>

        <p class="para">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet,
          animi Lorem ipsum dolor sit, amet consectetur adipisicing elit.
          Eveniet, animi.
        </p>
      </div>
    </SplideSlide>
    <SplideSlide class="container mx-auto">
      <div class="cardd">
        <img src="@/assets/5.png" alt="Sample 1" />
        <h1>Lorem, ipsum.</h1>
        <div class="new d-flex justify-content-between">
          <div class="d-flex">
            <i class="mt-1 mx-2 fa-solid fa-user-secret"></i>
            <p class="">ADMIN</p>
          </div>
          <div class="d-flex">
            <i class="mt-1 fa-solid fa-calendar-days"></i>
            <p class="mx-2">May,11-2023</p>
          </div>
        </div>

        <p class="para">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet,
          animi Lorem ipsum dolor sit, amet consectetur adipisicing elit.
          Eveniet, animi.
        </p>
      </div>
    </SplideSlide>
  </Splide>
</template>

<script>
import "@splidejs/vue-splide/css";

// or other themes
import "@splidejs/vue-splide/css/skyblue";
// or only core styles
import "@splidejs/vue-splide/css/core";
export default {
  data() {
    return {
      options: {
        perPage: 3,
        type: "loop",
        autoplay: true,
        interval: 3000,
        perMove: 1,
        pauseOnHover: true,
        pauseOnFocus: true,
        lazyLoad: true,
        arrows: true,
        pagination: true,
        focus: 0,

        breakpoints: {
          1400: {
            perPage: 2,
          },
          768: {
            perPage: 1,
          },
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.cardd {
  text-align: center;
  width: 350px;
  height: 500px;
  margin: 0 auto;
  box-shadow: 0 0 10px rgb(195, 195, 195);
  margin-bottom: 25px;

  img {
    width: 350px;
  }
}
@media screen and (max-width: 990px) {
  .cardd {
    text-align: center;
    width: 300px;
    margin: 0 auto;
    box-shadow: 0 0 10px rgb(195, 195, 195);
    margin-bottom: 25px;

    img {
      width: 300px;
    }
  }
}
p,
.d-flex {
}
.para {
  // max-width: 300px;
  // margin: 0 auto;
  text-align: start;
  margin: 0 18px;
}
.new {
  margin: 0 10px;
}
.h1 {
  margin-top: 100px;
  margin-bottom: 100px;
  text-transform: uppercase;
}
</style>
