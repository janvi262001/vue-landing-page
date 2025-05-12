<template>
    <section class="browse-categories">
      <div class="section-header">
        <h2>Browse by Categories</h2>
        <div class="filters">
            <button>All</button>
          <button v-for="(category, index) in categories" :key="index">{{ category.title }}</button>
\        </div>
      </div>
  
      <div class="cards-grid">
        <CategoryCard
          v-for="(category, index) in categories"
          :key="index"
          :image="category.image"
          :title="category.title"
        />
      </div>
    </section>
  </template>
  
  <script setup>
  import CategoryCard from './Reusable-components/CategoriesCards.vue'
  
  import menImg from '@/assets/images/men.jpeg'
  import womenImg from '@/assets/images/women.jpeg'
  import kidsImg from '@/assets/images/kids.jpeg'
  import accessoriesImg from '@/assets/images/accessories.jpeg'
  
  const categories = [
    { image: menImg, title: 'Men' },
    { image: womenImg, title: 'Women' },
    { image: kidsImg, title: 'Kids' },
    { image: accessoriesImg, title: 'Accessories' },
  ]
  </script>
  
  <style scoped>
  .browse-categories {
    padding: 2rem 1.5rem;
    max-width: 1200px;
    margin: auto;
  }
  
  .section-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.5rem;
    flex-wrap: wrap;
  }
  
  .section-header h2 {
    font-size: 1.75rem;
    font-weight: bold;
    color: #2c3e50;
  }
  
  .filters {
    display: flex;
    gap: 0.5rem;
  }
  
  .filters button {
    padding: 0.5rem 1rem;
    border: none;
    background: #eee;
    border-radius: 5px;
    cursor: pointer;
    font-weight: 500;
    transition: background 0.3s;
  }
  
  .filters button:hover {
    background: #ccc;
  }
  
  .cards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
  }
  </style>
  