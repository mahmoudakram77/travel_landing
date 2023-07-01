<template>
  <header class="position relative">
    <div class="dd"></div>
    <div class="blue" v-if="false">
      <p class="text-white">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium
        quisquam odit eaque exercitationem beatae magni optio laborum eligendi
        voluptatibus non.
      </p>
    </div>
    <div style="height: 25px" class="top-bar">
      <div class="content d-flex justify-content-between">
        <div class="contact d-flex">
          <i class="fa-solid fa-phone mt-2"></i>
          <p class="mt-1 mx-2">+970599085385</p>
          <i class="fa-solid fa-envelope mt-2"></i>
          <a
            style="color: white; text-decoration: none"
            class="mx-1 mt-1"
            href=""
            >mahmoudeljaru@gmail.com</a
          >
        </div>

        <div class="social d-flex">
          <div class="icon d-flex">
            <i
              style="color: rgb(48, 48, 160)"
              class="fa-brands fa-facebook-f"
            ></i>
            <i
              style="color: rgb(15, 167, 167)"
              class="fa-brands fa-twitter"
            ></i>
            <i
              style="color: rgb(45, 0, 103)"
              class="fa-brands fa-square-instagram"
            ></i>
            <i style="color: red" class="fa-brands fa-youtube"></i>
            <i style="color: green" class="fa-brands fa-whatsapp"></i>
          </div>
        </div>
      </div>
    </div>
    <content-header></content-header>
    <nav :class="{ 'fixed-navbar': isNavbarFixed }">
      <div class="nav-bar navnav">
        <div class="logo mb-1 mt-2">
          <img src="@/assets/logo.png" alt="" />
        </div>

        <ul v-show="!mobile">
          <li class="mt-3" v-for="menu in menus" :key="menu.id">
            <a class="link" :href="menu.url">{{ menu.name }}</a>
          </li>
        </ul>
      </div>

      <div
        class="burger"
        v-show="mobile"
        @click="toggleBurger"
        :class="{ 'icon-active': mobileNav }"
      >
        <span></span>
        <span></span>
        <span></span>
      </div>
      <transition name="down">
        <div class="bg" v-show="mobileNav">
          <ul class="mobile-nav">
            <li
              @click="toggleBurger"
              class="li-mobile"
              v-for="menu in menus"
              :key="menu.id"
            >
              <a class="link" :href="menu.url">{{ menu.name }}</a>

              <div class="line"></div>
            </li>
          </ul>
        </div>
      </transition>
    </nav>
  </header>
</template>
<script>
import contentHeader from "./contentHeader.vue";

export default {
  components: { contentHeader },
  data() {
    return {
      menus: [
        { id: 1, name: "home", url: "#" },
        { id: 2, name: "blog", url: "#" },
        { id: 3, name: "gallery", url: "#" },
        { id: 4, name: "articles", url: "#" },
        { id: 5, name: "deals", url: "#" },
        { id: 6, name: "contact", url: "#" },
      ],
      mobile: null,
      mobileNav: null,
      windowWidth: null,
      isNavbarFixed: false,
    };
  },

  methods: {
    toggleBurger() {
      this.mobileNav = !this.mobileNav;
    },
    checkScreen() {
      this.windowWidth = innerWidth;
      if (this.windowWidth <= 990) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
    },
    ScrollNavbar() {
      const navbar = this.$el.querySelector("nav");
      const navbarRect = navbar.getBoundingClientRect();
      const scrollPosition = window.scrollY || window.pageYOffset;
      this.isNavbarFixed = scrollPosition > navbarRect.top;
    },
  },
  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
    window.addEventListener("scroll", this.ScrollNavbar);
  },
};
</script>

<style lang="scss" scoped>
nav {
  transition: 0.5s ease all;
}
.fixed-navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 999;
  background: rgb(0, 0, 0);
  transition: 1s ease all;
  .burger {
    top: 12px;
  }
}
.top-bar {
  background: rgba(0, 0, 0, 0.566);
  color: white;
  padding: -5px 0;
  .content {
    margin: 0px 20px;
  }
  .social {
    .icon i {
      margin-right: 25px;
      margin-top: 5px;
      font-size: 20px;
      color: white;
    }
  }
}
.top-bar:after {
  content: "";
  display: block;
  width: 100%;
  height: 1px;
  background-color: white;
  position: absolute;
  top: 29px;
  opacity: 0.1;
}
.search:before {
  content: "";
  display: block;
  width: 3px;
  height: 30px;
  background-color: white;
  position: absolute;
  top: 0px;
  opacity: 0.1;
}
@media screen and (max-width: 768px) {
  .search:before {
    content: "";
    display: block;
    width: 3px;
    height: 29.7px;
    background-color: white;
    position: absolute;
    top: 0px;
    opacity: 0.1;
  }
}
header {
  background: url(@/assets/header.png);
  z-index: -1;
  height: 100vh;
  width: 100%;

  background-size: cover;
  background-position: center;
  nav {
    background: rgba(0, 0, 0, 0.566);
    width: 100%;
    .logo {
      z-index: 1;
    }

    ul {
      display: flex;
      list-style: none;

      li a {
        color: white;
        margin: 10px;
        text-decoration: none;
        text-transform: uppercase;
      }
    }
  }
}
@media screen and (max-width: 500px) {
  .blue {
    background: url(@/assets/header.png);
    bottom: 0;
    height: 1000px;
  }
}
.burger {
  z-index: 1;
  display: inline-block;
  cursor: pointer;

  span {
    width: 25px;
    height: 3px;
    display: block;
    background-color: white;
    margin: 5px 0;
    transition: transform 0.4s ease-in-out;
  }
  .social i {
    margin: 0;
  }
}
.icon-active span:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}
.icon-active span:nth-child(2) {
  opacity: 0;
}
.icon-active span:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}
.bg {
  background: black;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 0;
  top: 0;
  opacity: 0.8;
  .mobile-nav {
    display: flex;
    flex-direction: column;

    li {
      text-align: center;
      text-transform: uppercase;
      a {
      }
    }
  }
  li {
    margin-top: 50px;
  }
}

.down-enter-active {
  transition: 1s ease all;
}
.down-leave-active {
  transition: 1s ease all;
}
.down-enter-from {
  transform: translateY(-1000px);
}
.down-enter-to {
  transform: translateY(0px);
}
.down-leave-from {
  transform: translateY(0px);
}
.down-leave-to {
  transform: translateY(-1000px);
}
.line {
  width: 100%;
  height: 1px;
  opacity: 0.1;
  background-color: white;
  position: absolute;
  left: 50%;
  transform: translate(-50%);
  margin-top: 25px;
}

.burger {
  position: absolute;
  top: 40px;
  right: 50px;
}
@media screen and (max-width: 625px) {
  .top-bar {
    font-size: 12px;
  }
}
.icon {
  z-index: 3;
}
.content p,
i,
a {
  z-index: 3;
}
@media screen and (max-width: 991px) {
  .mobile-nav {
    margin-top: 50px;
  }
}
@media screen and (max-width: 543px) {
  .content {
    flex-direction: column;
    text-align: center;
    justify-content: center;
  }
  .contact {
    justify-content: flex-start;
    margin-left: 0px;
  }
  .icon,
  .social {
    justify-content: center;
    font-size: 15px;
  }
  .search {
    position: absolute;
    top: -5px;
    right: 20px;
    font-size: 20px;
  }
  nav {
    width: 100%;
  }
  .burger {
  }
  .search {
  }
  .blue p {
    text-align: center;
  }
  .search:before {
    content: "";
    display: block;
    width: 3px;
    height: 34px;
    background-color: white;
    position: absolute;
    top: 0px;
    opacity: 0.1;
  }
  .social {
  }
}

.blue {
  background: #4493e2;
  opacity: 0.8;
  width: 100%;
  height: 140px;
  position: absolute;
  bottom: 0%;
  display: flex;

  p {
    width: 500px;
    margin-top: 30px;
    padding-left: 20px;
    text-transform: capitalize;
    text-shadow: 5px 3px 5px black;
  }
}
@media screen and (max-width: 500px) {
  .logo {
    position: relative;
    left: -40px;
  }
  .burger {
    right: 25px;
  }
  .blue {
    height: 160px;
    p {
      margin-top: 0px;
    }
  }
  .social {
    .icon i {
      margin-right: -20px;
      margin-top: 5px;
      font-size: 20px;
      color: white;
    }
  }
}
@media screen and (max-width: 322px) {
  .search i {
    display: none;
  }
  .search::before {
    display: none;
  }
}
.navnav {
  display: flex;
  justify-content: space-between;
  // margin: 0 60px;
}
.nav-bar {
  display: flex;
  justify-content: space-between;
  align-items: center; /* لمحاذاة العناصر عموديًا في الوسط */
  margin: 0 60px;
}
.link {
  position: relative;
  display: inline-block;
  &::after {
    content: "";
    display: block;
    position: absolute;
    top: -2px;
    width: 0;
    left: 0;
    height: 3px;
    background-color: white;
    transition: width 0.3s;
  }
  &:hover::after {
    width: 100%;
  }
}
@media screen and (max-width: 500px) {
  .social {
    margin-left: 20px;
  }
}
.social {
  cursor: pointer;
}
</style>
