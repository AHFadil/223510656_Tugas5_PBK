<template>
    <div class="card">
      <img :src="image" alt="Product Image" class="card-img">
      <div class="card-body">
        <h3>{{ title }}</h3>
        <p>{{ description }}</p>
      </div>
    </div>
</template>
  
<script setup>
  defineProps({
    image: String,
    title: String,
    description: String
  });
</script>
  
<style scoped>
  .card {
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.2s;
  }
  .card:hover {
    transform: translateY(-5px);
  }
  .card-img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  .card-body {
    padding: 1rem;
  }
</style>
  