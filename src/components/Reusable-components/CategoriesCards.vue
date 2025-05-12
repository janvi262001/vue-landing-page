<template>
    <div class="category-card">
      <img :src="image" :alt="title" />
      <div class="card-title">{{ title }}</div>
    </div>
  </template>
  
  <script setup>
  defineProps({
    image: String,
    title: String,
  })
  </script>
  
  <style scoped>
  .category-card {
    border-radius: 8px;
    overflow: hidden;
    text-align: center;
    background: #f8f8f8;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
    transition: transform 0.3s;
  }
  
  .category-card:hover {
    transform: translateY(-5px);
  }
  
  .category-card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
  }
  
  .card-title {
    padding: 0.75rem;
    font-weight: 600;
    color: #2c3e50;
  }
  </style>
  