<template>
  <div class="home">
    <Navbar msg="Welcome to Your Vue.js App" />
    <div class="container">
      <Hero />

      <div class="row mt-4">
        <div class="col">
          <h2>
            Best
            <strong>Foods</strong>
          </h2>
        </div>
        <div class="col">
          <router-link to="/foods">
            <button class="btn btn-success float-right">
              <b-icon-eye></b-icon-eye>Lihat Semua
            </button>
          </router-link>
        </div>
      </div>

      <div class="row mb-3">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id" >
          <CardProduct :product="product" />
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProduct from "@/components/Card.vue"
import axios from "axios"

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    CardProduct
  },
  data() {
    return{
      products: [],
    }
  },
  methods: {
    setProduct(data) {
      this.products = data
    }
  },
  mounted() {
    axios.get('http://localhost:3000/best-products')
    .then((response) => this.setProduct(response.data))
    .catch((error) => console.log(error))
  }
};
</script>
