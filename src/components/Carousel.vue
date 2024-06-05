<template>
    <div class="carousel">
      <div class="carousel-inner" :style="{ transform: `translateX(-${currentSlide * 100}%)` }">
        <div class="carousel-item" v-for="(image, index) in images" :key="index">
          <img :src="image" alt="Carousel Image">
        </div>
      </div>
    </div>
</template>
  
<script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const images = [
    'https://images.tokopedia.net/img/cache/1200/BgtCLw/2023/11/8/9796b7f4-3804-45e5-b46a-339888c09ab5.jpg.webp?ect=4g',
    'https://assets.website-files.com/5fc9d3d58a00611de699385c/5fdc6b2c4212759d3a0410c6_15.png',
    'https://cdn0-production-images-kly.akamaized.net/tElOwOVXT6KmvynhuMXq8yaYHQ8=/800x450/smart/filters:quality(75):strip_icc():format(webp)/kly-media-production/medias/853262/original/006515100_1429161283-gtavreviewheader.jpg'
  ];
  
  const currentSlide = ref(0);
  const totalSlides = images.length;
  
  let intervalId;
  
  const nextSlide = () => {
    currentSlide.value = (currentSlide.value + 1) % totalSlides;
  };
  
  onMounted(() => {
    intervalId = setInterval(nextSlide, 3000);
  });
  
  onUnmounted(() => {
    clearInterval(intervalId);
  });
</script>
  
<style scoped>
  .carousel {
    max-width: 100%;
    margin: auto;
    overflow: hidden;
    position: relative;
  }
  .carousel-inner {
    display: flex;
    transition: transform 0.5s ease;
  }
  .carousel-item {
    min-width: 100%;
    box-sizing: border-box;
  }
  .carousel img {
    width: 100%;
    height: 400px;
    object-fit: cover;
  }
</style>
  