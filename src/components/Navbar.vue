<template>
    <nav class="navbar">
      <div class="navbar-container">
        <div class="left-section">
          <router-link to="/" class="logo">MyShop</router-link>
          <ul :class="['nav-links', { 'open': isMenuOpen }]">
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/shop">Shop</router-link></li>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/contact">Contact</router-link></li>
          </ul>
        </div>
  
        <div class="right-section">
          <button class="icon-btn" title="Search">🔍</button>
          <button class="icon-btn" title="Cart">🛒</button>
          <button class="icon-btn" title="Wishlist">❤️</button>
          <button class="icon-btn" title="Profile">👤</button>
  
          <button class="hamburger" @click="isMenuOpen = !isMenuOpen">
            <span :class="{ open: isMenuOpen }"></span>
            <span :class="{ open: isMenuOpen }"></span>
            <span :class="{ open: isMenuOpen }"></span>
          </button>
        </div>
      </div>
    </nav>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  const isMenuOpen = ref(false)
  </script>
  
  <style scoped>
  .navbar {
    background-color: #fff;
    border-bottom: 1px solid #eaeaea;
    padding: 0.75rem 1.5rem;
    position: sticky;
    top: 0;
    z-index: 999;
  }
  
  .navbar-container {
    max-width: 1200px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .left-section {
    display: flex;
    align-items: center;
    gap: 2rem;
  }
  
  .logo {
    font-size: 1.6rem;
    font-weight: bold;
    color: #333;
    text-decoration: none;
  }
  
  .nav-links {
    display: flex;
    gap: 1.5rem;
    list-style: none;
  }
  
  .nav-links li a {
    text-decoration: none;
    color: #333;
    font-weight: 500;
    transition: color 0.2s;
  }
  
  .nav-links li a:hover {
    color: #007bff;
  }
  
  .right-section {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  
  .icon-btn {
    background: none;
    border: none;
    font-size: 1.2rem;
    cursor: pointer;
    transition: transform 0.2s;
  }
  
  .icon-btn:hover {
    transform: scale(1.2);
  }
  
  .hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    background: none;
    border: none;
    cursor: pointer;
  }
  
  .hamburger span {
    width: 24px;
    height: 3px;
    background-color: #333;
    border-radius: 2px;
    transition: all 0.3s;
  }
  
  .hamburger span.open:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
  }
  .hamburger span.open:nth-child(2) {
    opacity: 0;
  }
  .hamburger span.open:nth-child(3) {
    transform: rotate(-45deg) translate(5px, -5px);
  }
  
  @media (max-width: 768px) {
    .nav-links {
      position: absolute;
      top: 64px;
      left: 0;
      width: 100%;
      background-color: #fff;
      flex-direction: column;
      padding: 1rem;
      border-top: 1px solid #eee;
      display: none;
    }
  
    .nav-links.open {
      display: flex;
    }
  
    .hamburger {
      display: flex;
    }
  
    .left-section {
      gap: 1rem;
    }
  
    .nav-links li {
      text-align: center;
      padding: 0.5rem 0;
    }
  }
  </style>
  