<template>
  <div class="BeritaView">
    <NavbarComponent />

    <section class="section">
      <div class="container">
        <!-- berita -->
        <div class="row mt-4">
          <div class="col">
            <h2>
              <strong>Berita Terkini</strong>
            </h2>
          </div>
        </div>

        <!-- Belum ada backend -->
        <div class="row mb-4">
          <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
            <BeritaTerkini :product="product" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarComponent from '@/components/NavbarComponent.vue';
import BeritaTerkini from '@/components/BeritaTerkini.vue';
import axios from 'axios';

export default {
  name: 'BeritaView',
  components: {
    NavbarComponent,
    BeritaTerkini,
  },

  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get('https://67e3b96c2ae442db76d1464f.mockapi.io/latihan/v1/article')
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style></style>
