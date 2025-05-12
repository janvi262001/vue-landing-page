<template>
    <div class="product-card">
      <img :src="image" :alt="name" />
      <div class="product-info">
        <h3 class="product-name">{{ name }}</h3>
        <div class="product-details">
          <span class="rating">⭐ {{ rating }}</span>
          <span class="price">${{ price }}</span>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  defineProps({
    image: String,
    name: String,
    rating: Number,
    price: Number,
  })
  </script>
  
  <style scoped>
  .product-card {
    background: #fff;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s;
    cursor: pointer;
  }
  
  .product-card:hover {
    transform: translateY(-5px);
  }
  
  .product-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  
  .product-info {
    padding: 0.75rem;
  }
  
  .product-name {
    font-size: 1rem;
    margin: 0 0 0.5rem;
    color: #2c3e50;
  }
  
  .product-details {
    display: flex;
    justify-content: space-between;
    font-size: 0.9rem;
    color: #666;
  }
  </style>
  