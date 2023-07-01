<template>
  <Splide :options="options2" aria-label="My Favorite Images">
    <SplideSlide>
      <h1>Lorem, ipsum dolor.</h1>
      <h5>Lorem ipsum dolor sit amet.</h5>
    </SplideSlide>
    <SplideSlide>
      <h1>new new new</h1>
      <h5>Lorem ipsum dolor sit amet.</h5>
    </SplideSlide>
    <SplideSlide>
      <h1>Lorem, lorem lorem</h1>
      <h5>Lorem ipsum dolor sit amet.</h5>
    </SplideSlide>
  </Splide>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
export default {
  components: {
    Splide,
    SplideSlide,
  },
  data() {
    return {
      options2: {
        perMove: 1,
        pagination: false,
        arrows: false,
        type: "loop",
        autoplay: true,
        interval: 2000,
        pauseOnHover: false,
        waitForTransition: true,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
h1,
h5 {
  color: white;
}
</style>
