<template>
  <div>
    <div class="bg position-relative">
      <div class="footer text-center">
        <!-- splid -->
        <splide-footer></splide-footer>
        <div class="circle">
          <h1>FIND TOUR</h1>
        </div>
      </div>
    </div>
    <div class="bg2">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-xxl-3 col-sm-12">
            <h1 class="mb-4 mt-3">findfinder llc</h1>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet
              repellat vitae velit, minima iste dolorum laudantium reiciendis
              magnam. Ipsum, aut.
            </p>
          </div>
          <div class="col-xxl-3 col-sm-12">
            <h1 class="mb-4 mt-3">support</h1>
            <ul class="one">
              <li>faq</li>
              <li>payment option</li>
              <li>booking tips</li>
            </ul>
          </div>
          <div class="col-xxl-3 col-sm-12">
            <h1 class="mb-4 mt-3">follow us</h1>
            <div class="ss">
              <ul class="social">
                <li class="">
                  <a href=""><i class="fa-brands fa-facebook"></i></a>
                </li>
                <li class="">
                  <a href=""
                    ><i style="color: aqua" class="fa-brands fa-twitter"></i
                  ></a>
                </li>
                <li>
                  <a href="">
                    <i style="color: red" class="fa-brands fa-youtube"></i>
                  </a>
                </li>
                <li class="">
                  <a href=""
                    ><i
                      style="color: darkblue"
                      class="fa-brands fa-square-instagram"
                    ></i
                  ></a>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-xxl-3 col-sm-12">
            <h1 class="mb-5 mt-3">newsletter</h1>
            <div class="d-flex ii">
              <input type="text" class="" placeholder="enter your email" />
              <button class="btnn">Submit</button>
            </div>
          </div>
          <div class="mb-3 mt-5">design and develop by mahmoud eljaru</div>
          <div class="mb3">copyright 2023</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SplideFooter from "./splideFooter.vue";
// Default theme

export default {
  components: { SplideFooter },
  data() {
    return {
      options2: {
        perMove: 1,
        pagination: false,
        arrows: false,
        type: "loop",
        autoplay: true,
        interval: 3000,
        pauseOnHover: false,
        waitForTransition: true,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
* {
  // overflow: hidden;
}
.bg {
  margin-top: 100px;
  overflow: hidden;
}
footer {
  position: absolute;
  bottom: 0px;
}
.footer {
  background-image: url(../assets/16.png);
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 70vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  h1 {
    color: white;
  }
  p {
    color: white;
  }
}
.circle {
  width: 120px;
  height: 120px;
  background: rgb(35, 21, 237);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  color: white;
  font-weight: bolder;
  box-shadow: 0 0 20px white;
  transition: 1s ease all;
  text-shadow: 0 0 10px black;
  h1 {
    font-size: 18px;
    animation: movve 3s infinite alternate;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  cursor: pointer;
  &:hover {
    transform: scale(1.1);
    transition: 0.3ease all;
  }
}
@keyframes movve {
  0% {
    letter-spacing: 0px;
  }
  100% {
    letter-spacing: 1px;
  }
}
.container {
  margin-top: 100px;
  h1 {
    text-transform: uppercase;
  }
  p,
  a,
  li {
    text-transform: capitalize;
  }
  ul {
    list-style: none;
  }
}
.social {
  display: flex;
  i {
    font-size: 40px;
  }
}
ul {
  margin: 0;
  padding: 0;
}
li {
  margin-bottom: 0;
}
a {
  margin-right: 10px;
}
@media screen and (max-width: 768px) {
  .row {
    margin: 0 auto;
    text-align: center;
  }
  ul li a {
    margin: 0 auto;
    text-align: center;
  }
  .ss {
    display: flex;
    justify-content: center;
    align-items: center;
    ul {
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
  .ii {
    justify-content: center;
  }
}
.col-xxl-3 {
  h1 {
    font-size: 25px;
  }
}
input {
  width: 250px;
}
p {
  max-width: 450px;
}
.container {
  color: white;
  text-shadow: 1px 2px 8px rgb(255, 255, 255);
}
.bg2 {
  background: rgba(0, 0, 0, 0.953);
  padding: 1px;
  height: 100%;
}
.btnn {
  background: blue;
  border: blue;
  border-radius: 0 10px 10px 0;
}
input {
  border-radius: 10px 0 0 10px;
  border: none;
  outline: none;
}
</style>
