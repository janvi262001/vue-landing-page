<template>
    <section class="popular-products">
      <h2>Popular Products</h2>
      <div class="products-grid">
        <ProductCard
          v-for="(product, index) in products"
          :key="index"
          :image="product.image"
          :name="product.name"
          :rating="product.rating"
          :price="product.price"
        />
      </div>
    </section>
  </template>
  
  <script setup>
  import ProductCard from './Reusable-components/ProductCard.vue'
  
  import product1 from '@/assets/images/product1.jpeg'
  import product2 from '@/assets/images/product2.jpeg'
  import product3 from '@/assets/images/product3.jpeg'
  import product4 from '@/assets/images/product4.jpeg'
  
  const products = [
    { image: product1, name: 'girls tshirt', rating: 4.5, price: 29.99 },
    { image: product2, name: 'girls tshirt', rating: 4.2, price: 49.99 },
    { image: product3, name: 'women tshirt', rating: 4.8, price: 89.99 },
    { image: product4, name: 'men tshirt', rating: 4.4, price: 39.99 },
    { image: product1, name: 'girls tshirt', rating: 4.5, price: 29.99 },
    { image: product2, name: 'girls tshirt', rating: 4.2, price: 49.99 },
    { image: product3, name: 'men tshirt', rating: 4.8, price: 89.99 },
    { image: product4, name: 'women tshirt', rating: 4.4, price: 39.99 },
    { image: product1, name: 'girls Fit tshirt', rating: 4.5, price: 29.99 },
    { image: product2, name: 'girls tshirt', rating: 4.2, price: 49.99 },
    { image: product3, name: 'women tshirt', rating: 4.8, price: 89.99 },
    { image: product4, name: 'men tshirt', rating: 4.4, price: 39.99 },
  ]
  </script>
  
  <style scoped>
  .popular-products {
    padding: 2rem 1.5rem;
    max-width: 1200px;
    margin: auto;
  }
  
  .popular-products h2 {
    font-size: 1.75rem;
    font-weight: bold;
    color: #2c3e50;
    margin-bottom: 1.5rem;
  }
  
  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
  }
  </style>
  