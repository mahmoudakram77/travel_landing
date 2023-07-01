<template>
  <top-bar></top-bar>
  <nav-bar></nav-bar>
  <sec-two></sec-two>
  <sec-three></sec-three>
  <sec-four></sec-four>
  <search-modal></search-modal>
  <card-caruosel></card-caruosel>
  <footer-sec></footer-sec>
  <scroll-top></scroll-top>
</template>

<script>
import CardCaruosel from "./components/cardCaruosel.vue";
import FooterSec from "./components/footerSec.vue";
import NavBar from "./components/navBar.vue";
import ScrollTop from "./components/ScrollTop.vue";
import SearchModal from "./components/searchModal.vue";
import SecFour from "./components/secFour.vue";
import SecThree from "./components/secThree.vue";
import SecTwo from "./components/secTwo.vue";
import TopBar from "./components/topBar.vue";
export default {
  name: "App",
  components: {
    TopBar,
    NavBar,
    FooterSec,
    ScrollTop,
    SecTwo,
    SecThree,
    SecFour,
    SearchModal,
    CardCaruosel,
  },
};
</script>

<style lang="scss">
body {
}
* {
  text-transform: uppercase;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
