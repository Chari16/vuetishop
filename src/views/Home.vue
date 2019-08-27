<template>
  <div class="home-component">
    <carousel :per-page="1" :navigate-to="someLocalProperty" :mouse-drag="false">
      <slide>
        <img style="width:100%;height: 320px;" src="https://img.global.news.samsung.com/in/wp-content/uploads/2018/03/PR_1242x400_banner2.jpg">
      </slide>
      <slide>
        <img style="width:100%;height: 320px;" src="https://rukminim1.flixcart.com/flap/844/140/image/8c2981a2d2e3afde.jpg">
      </slide>
    </carousel>
    <!-- <div class="jumbotron jumbotron-fluid">
        <div class="container">
          <img alt="Vue logo" src="../assets/logo.png" width="100px">
          <h3 class="display-5 "><span style="color:#42b983">Bhavesh - VueShop</span></h3>
          <p class="lead">A ShoppingCart (Ecommerce) Application using Vue.js.</p>
        </div>
    </div> -->
    <nav aria-label="breadcrumb">
      <ol class="breadcrumb">
        <li class="breadcrumb-item active" aria-current="page">Our Best Products</li>
        <li class="ml-auto" aria-current="page"><router-link to="/products">Show All</router-link></li>
      </ol>
      
    </nav>
    <BestProducts></BestProducts>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import BestProducts from "@/components/products/BestProducts.vue";
import { Carousel, Slide } from 'vue-carousel';
export default {
  name: "home",
  components: {
    HelloWorld,
    BestProducts,
    Carousel,
    Slide
  }
};
</script>
<style>
.jumbotron {
  padding: 1rem 0rem;
}
</style>
