<template>
  <div class="home">
    <Navbar />
    <!-- <h1>This is the home page</h1> -->
    <!-- <div id="carouselExampleFade" class="carousel slide carousel-fade" data-bs-ride="carousel">

  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="images/room.jpg" class="d-block w-100" alt="hospital room">
    </div>
    <div class="carousel-item">
      <img src="images/group.jpg" class="d-block w-100" alt="group of doctors">
    </div>
    <div class="carousel-item">
      <img src="images/cancer.jpg" class="d-block w-100" alt="cancer group">
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div> -->
    <div class="container-fluid banner-holder">
      <!-- <div class="container"> -->
        <div class="row" style="height:100%">
          <div class="col-md-12 col-sm-12 text-image-part text-center">
            <div class="row" style="height:100%;">
            <div class="col-md-7 col-sm-12 text-part">
            <h3>H<span>M</span>S</h3>
            <h1>here to serve you better</h1>
            <!-- <input type="submit" class="start-btn btn" value="Get Started"> -->
            <router-link to="/register" class="start-btn btn">Get Started</router-link>
            </div>
            <!-- <div class="col-md-7 image-part">

            </div> -->
            </div>
          </div>
          
        </div>
      </div>
      <!-- <i class="fa fa-eye" style = "font-size:400px; color:black;"></i> -->
      <section id="info">
        <i class="fa fa-home fa-4x"></i>
      </section>
    </div>
  <!-- </div> -->
</template>

<script>
// @ is an alias to /src
import Navbar from "../components/Navbar.vue";

export default {
  name: "Home",
  components: {
    Navbar,
  },
};
</script>

<style scoped lang="scss">
.banner-holder {
  width: 100%;
  height: calc(700px - 88px);
}
.text-image-part{
  height: 100%;
  width: 100%;
  background: radial-gradient(rgba(148, 148, 153, 0.7), rgba(24, 26, 46, 0.849)), url(/images/group.jpg) no-repeat center center/cover;

}
.image-part{
  height: 100%;

}
.start-btn{
  padding: 10px 15px;
  background-color: #398cebd3;
  color: #fff;
  font-weight: bold;
  text-transform: capitalize;
  border: 1px solid #fff;
  font-size: 20px;
}
.start-btn:hover{
  background-color: #1366c5d3;
}

.text-part{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;


  h3{
    color: white;
    font-size: 38px;
    font-weight: bold;

    span{
      color: #fff ;
    }
  }
  h1{
    color: white;
    text-transform: uppercase;
    font-size: 60px;
    color: #fff;
    font-weight: bold;

  }
}
// @media (max-width:800px){
//   .text-part{
    
//     h1{
//       color:red;
//     }
    
//   }
// }
</style>
