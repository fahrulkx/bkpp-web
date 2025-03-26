<template>
  <div class="card">
    <img :src="'asset/img/' + product.image" class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ product.title }}</h5>
      <p class="card-text">{{ product.body }}</p>
      <a href="#" class="btn btn-success">Baca selengkapnya</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BeritaTerkini',
  props: ['product'],
};
</script>

<style></style>
