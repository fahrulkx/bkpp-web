<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">{{ product.title }}</h5>
      <h6 class="card-subtitle mb-2 text-body-secondary">{{ product.tanggal }}</h6>
      <p class="card-text">{{ product.body }}</p>
      <a href="#" class="btn btn-success">Baca selengkapnya</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PengumumanComponent',
  props: ['product'],
};
</script>

<style></style>
