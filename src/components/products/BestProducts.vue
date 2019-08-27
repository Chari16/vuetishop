<template>
  <div class="best-products">
    <div class="row">
      <!-- <card-loader :loopCount="4" v-if="loading"/> -->
      <div class="col-md-6" v-for="(item, index) in bestProducts" :key="index">
        <card-template :item="item"/>
      </div>
    </div>
  </div>
</template>

<script>
// import CardLoader from '../shared/CardLoader'
import CardTemplate from '../shared/CardTemplate'
export default {
  name: "BestProducts",
  components: { CardTemplate},
  data() {
    return {
      loading:true,
      bestProducts:[{
        isBestProduct: true,
        isTopProduct: true,
        productCategory: "Smartphone",
        productDescription: "Camera: 13 MP Rear camera with Fast facial unlock in less than 0.1 second with AI Recognition | 8 MP front camera Display: 15.24 centimeters (6-inch) Full HD In-cell capacitive touchscreen display with 2160x1080 pixels",
        productImage: "https://images-na.ssl-images-amazon.com/images/I/616-sGx5LTL._SY879_.jpg",
        productName: "RealMe 1 (Black, 6GB RAM, 128GB Storage)",
        productPrice: "11,999.00",
        productRating: 4.9,
        productSeller: "Realme",
        __v: 0,
        _id: "5bd44827429e8654fc8e5a4c",
      },{
        isBestProduct: true,
        isTopProduct: false,
        productCategory: "Smartphone",
        productDescription: "Camera: 12+12 MP Dual rear Camera with Autofocus, 2x Optical zoom | 8 MP front camera with Image recording, Touch focus and Face smile detection Display: 16.05 centimeters (6.3-inch) QHD+ capacitive touchscreen display with 1440x2960 pixels, 521 ppi pixel density and 18.5:9 aspect ratio",
        productImage: "https://images-na.ssl-images-amazon.com/images/I/815Aay6NVhL._SY879_.jpg",
        productName: "Samsung Galaxy Note 8 (Midnight Black, 6GB RAM, 64GB Storage)",
        productPrice: "43,990.00",
        productRating: 4.5,
        productSeller: "Samsung",
        __v: null,
        _id: "5bd4640589d37528b8eba255"
      },
      {
        isBestProduct: true,
        isTopProduct: true,
        productCategory: "Smartphone",
        productDescription: "Camera: 13 MP Rear camera with f1.9 with Auto focus and Rear flash | 13 MP front camera Display: 13.88 centimeters (5.5-inch) Full HD display with 1080x1920 pixels | 2.5D Gorilla Glass Memory, Storage & SIM: 4GB RAM | 64GB storage expandable up to 256GB | Dual nano SIM with dual standby (4G+3G)",
        productImage: "https://images-na.ssl-images-amazon.com/images/I/61EM4uS-5iL._SY879_.jpg",
        productName: "Samsung Galaxy On7 Prime (Black, 4GB RAM, 64GB Storage)",
        productPrice: "10,990.00",
        productRating: 3.5,
        productSeller: "Samsung",
        __v: null, 
        _id: "5bd4659e89d37528b8eba256"
      },
      {
        isBestProduct: true,
        isTopProduct: true,
        productCategory: "Smartphone",
        productDescription: "Camera: 12+12 MP Dual rear camera with Dual optical image stabilization, Portrait Mode, Digital zoom up to 10x, Quad-LED True tone flash and Slow sync, 4K Video recording at 24 fps or 30 fps or 60 fps and Slow-motion video recording in 1080p at 120 fps | 7 MP front TrueDepth camera with Retina Flash and Animoji feature",
        productImage: "https://images-na.ssl-images-amazon.com/images/I/61682XpNGFL._SY879_.jpg",
        productName: "Apple iPhone X (Space Grey, 3GB RAM, 64GB Storage)",
        productPrice: "74,999.00",
        productRating: 5,
        productSeller: "Apple",
        __v: null,
        _id: "5bd4712c89d37528b8eba25a"
      }
      ],
    };
  },
};
</script>

<style>
.best-products {
  margin-bottom: 10px;
}
</style>
