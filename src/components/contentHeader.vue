<template>
  <div class="container con">
    <div class="row">
      <div class="col-lg-8 col-sm-12 one">
        <h2 class="display-2 text-white shadow">where your journey begins</h2>

        <h5 class="mt-3">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Fugit,
          maxime! Lorem ipsum dolor, sit amet consectetur adipisicing elit.
        </h5>
      </div>

      <div class="col-lg-4 col-sm-12 form" style="color: white">
        <form class="mx-auto text-center">
          <label style="font-size: 30px" for="">SEARCH TOURS</label>
          <p style="font-size: 13px">FIND TOUR DREAM HOUR TODAY</p>
          <div class="in position-relative">
            <input placeholder="search" class="" type="text" />
            <i class="fas fa-search"></i>
          </div>
          <div class="in position-relative">
            <input placeholder="destination" class="" type="text" />
            <i class="fa-solid fa-plane-departure"></i>
          </div>
          <div class="in position-relative">
            <input placeholder="destination" class="" type="text" />
            <i class="fa-solid fa-bed"></i>
          </div>
          <div class="in position-relative">
            <input placeholder="destination" class="" type="text" />
            <i class="fa-solid fa-calendar-days"></i>
          </div>
          <button class="text-center btn btn-primary">FIND TOURS</button>
        </form>
      </div>
    </div>
  </div>
  <div v-if="false">
    <i class="fas fa-search"></i>
    <i class="fa-solid fa-plane-departure"></i>
    <i class="fa-solid fa-bed"></i>
    <i class="fa-solid fa-calendar-days"></i>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.con {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  .one {
    h1 {
      color: white;
      text-transform: capitalize;
    }
    h5 {
      // max-width: 480px;
      text-transform: capitalize;
      color: white;
    }
  }
}
h2 {
  animation: color 5s infinite alternate;
}
@keyframes color {
  0% {
    text-shadow: 0 0 10px #4493e2;
  }
  50% {
    text-shadow: #98cafb;
  }
  100% {
    text-shadow: 0 0 10px rgb(0, 225, 255);
  }
}

button,
input {
  width: 240px;
  border-radius: 5px;
  border: none;
}
.in i {
  position: absolute;
  right: 40px;
  top: 10px;
}
input {
  border: 2px solid #000000;
  padding: 5px 10px;
  font-size: 16px;
  transition: border-color 0.5s;
}
input:hover {
  border-color: #939393;
}
input:focus {
  border-color: #333;
  box-shadow: 0 0 5px #333;
  outline: none;
}
.row {
  align-items: center;
}
.form form {
  width: 320px;
  height: 320px;
}
.in {
  margin-bottom: 5px;
}

.con {
  overflow-x: hidden;
}
form {
  background: white;
  background-size: cover;
  background-position: center;
  padding: 10px;
  color: #000000;
  font-weight: bolder;
  box-shadow: 0 0 10px black;
  border-radius: 2px;
}
@media screen and (max-width: 360px) {
  .form form {
    width: 250px;
    input,
    button {
      width: 180px;
    }
  }
}
@media screen and (max-width: 600px) {
  .one h1 {
    color: red;
    display: none;
  }
  .form form {
    margin-top: 50px;
  }
  .one {
    margin-top: 80px;
  }
}
@media screen and (max-width: 991px) {
  .one {
    text-align: center;
    h5 {
      font-size: 18px;
      text-align: center;
    }
    h1 {
    }
  }
  .form {
    margin-top: 15px;
  }
}
</style>
