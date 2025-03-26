<template>
  <div class="home">
    <NavbarComponent />
    <HeroSection />

    <section class="section">
      <div class="container">
        <!-- berita -->
        <div class="row mt-4">
          <div class="col">
            <h2>
              <strong>Berita Terkini</strong>
            </h2>
          </div>
          <div class="col">
            <router-link to="/BeritaView" class="btn btn-success float-end"> <i class="bi bi-eye"></i> Lihat Semua </router-link>
          </div>
        </div>

        <div class="row mb-4">
          <div class="col-md-4 mt-4">
            <BeritaTerkini />
          </div>
        </div>
      </div>
    </section>

    <section class="section light-background">
      <div class="container">
        <!-- Pengumuman -->
        <div class="row mt-4">
          <div class="col">
            <h2>
              <strong>Pengumuman</strong>
            </h2>
          </div>
          <div class="col">
            <router-link to="/" class="btn btn-success float-end"> <i class="bi bi-eye"></i> Lihat Semua </router-link>
          </div>
        </div>

        <div class="row mb-4">
          <div class="col-md-12 mt-4">
            <PengumumanComponent />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarComponent from '@/components/NavbarComponent.vue';
import HeroSection from '@/components/HeroSection.vue';
import BeritaTerkini from '@/components/BeritaTerkini.vue';
import PengumumanComponent from '@/components/PengumumanComponent.vue';

export default {
  name: 'HomeView',
  components: {
    NavbarComponent,
    HeroSection,
    BeritaTerkini,
    PengumumanComponent,
  },
  data() {
    return {
      products: [],
    };
  },
};
</script>
