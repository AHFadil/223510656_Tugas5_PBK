<template>
    <nav class="navbar">
      <div class="container">
        <a href="#" class="logo">AhmadFadil</a>
        <ul class="nav-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">Products</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>
    </nav>
</template>
  
<script setup>
</script>
  
<style scoped>
  .navbar {
    background: #333;
    color: #fff;
    padding: 1rem;
  }
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .nav-links {
    list-style: none;
    display: flex;
  }
  .nav-links li {
    margin-left: 1rem;
  }
  .nav-links a {
    color: #fff;
    text-decoration: none;
  }
  .logo {
    text-decoration: none;
    color: white;
  }
</style>
  