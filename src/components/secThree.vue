<template>
  <div class="overlay">
    <div class="container-fluid">
      <div class="row d-flex">
        <div
          class="text-center display-3 text-white mt-5"
          data-aos="fade-up"
          data-aos-duration="1000"
        >
          Lorem, ipsum dolorr.
        </div>
        <div
          class="col-lg-4 col-md-4 col-sm-12 coco position-relative mt-5"
          v-for="infom in infoms"
          :key="infom.id"
        >
          <div
            class="cardd text-center"
            data-aos="zoom-in"
            data-aos-duration="2000"
          >
            <img
              class="img-fluid"
              src="https://static.toiimg.com/thumb/msid-92344744,width-748,height-499,resizemode=4,imgsize-39674/.jpg"
              alt=""
            />
            <div class="bg bg-white">
              <h2 class="price">&#36;{{ infom.price }}</h2>
              <h1 class="title pt-5">{{ infom.title }}</h1>
              <p class="para text-black-50">
                {{ infom.para }}
              </p>
              <button>BOOK NOW</button>
            </div>
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
      infoms: [
        {
          id: 1,
          price: 100,
          title: "lorem lorem",
          para: " Lorem ipsum dolor sit, amet consectetur adipisicing elit",
        },
        {
          id: 2,
          price: 100,
          title: "lorem lorem",
          para: " Lorem ipsum dolor sit, amet consectetur adipisicing elit",
        },
        {
          id: 3,
          price: 100,
          title: "lorem lorem",
          para: " Lorem ipsum dolor sit, amet consectetur adipisicing elit",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
* {
}
.overlay {
  // background-image: url("@/assets/Layer17.png");
  background-color: rgb(0, 123, 255);
  height: 100vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
}
.cardd {
  width: 300px;
  box-shadow: 0 0 40px rgba(244, 244, 244, 0.3);
  border-radius: 20px 20px 20px 20px;
  border: none;
}
.coco {
}
img {
  width: 300px;
  height: 200px;
}
button {
  margin-bottom: 10px;
}
.price {
  background: rgb(55, 80, 247);
  display: inline-block;
  padding: 5px 15px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
@media screen and (max-width: 768px) {
  .col-lg-3 {
    margin-left: auto;
    margin-right: auto;
    display: flex;
    justify-content: center;
  }

  .overlay {
    height: 1550px;
    background-position: center;
    background-size: cover;
  }
}
button {
  background: blue;
  border: none;
  color: white;
  font-weight: bolder;
  padding: 10px 20px;
  transition: 0.5s ease all;
  border-radius: 5px;
  &:hover {
    background: rgba(0, 0, 255, 0.741);
    transition: 0.5s ease all;
  }
}
.col-lg-4 {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  top: 20px;
}
.cardd {
  width: 320px;

  img {
    width: 320px;
    border-radius: 20px 20px 0 0;
  }
  .bg {
    border-radius: 0 0 20px 20px;
  }
}
</style>
