<template>
  <section class="main-banner">
    <!-- Top Banner -->
    <div class="top-banner">
      <div class="slogan">
        <h1>Elevate your wardrobe<br />with irresistible fashion finds!</h1>
      </div>
      <div class="reviews">
        <p class="review-text">
          You’ll discover a world of style at <strong>Silasya</strong>, where fashion meets comfort.
        </p>
        <div class="user-info">
          <div class="user-images">
            <img :src="user1" alt="User 1" />
            <img :src="user2" alt="User 2" />
            <img :src="user3" alt="User 3" />
          </div>
          <div class="user-count">20K+ Satisfied Users</div>
        </div>
      </div>
    </div>

    <!-- Lower Section: Image Grid -->
    <div class="image-grid">
      <div class="left-block">
        <img :src="fashion1" alt="Fashion 1" class="top-img" />
        <div class="bottom-row">
          <img :src="fashion2" alt="Fashion 2" />
          <img :src="fashion3" alt="Fashion 3" />
        </div>
      </div>
      <div class="right-block">
        <img :src="fashion4" alt="Fashion 4" />
      </div>
    </div>
  </section>
</template>

<script setup>
import user1 from '@/assets/images/user1.jpeg'
import user2 from '@/assets/images/user2.jpeg'
import user3 from '@/assets/images/user3.png'
import fashion1 from '@/assets/images/fashion1.jpeg'
import fashion2 from '@/assets/images/fashion2.jpeg'
import fashion3 from '@/assets/images/fashion3.jpeg'
import fashion4 from '@/assets/images/fashion4.avif'
</script>

<style scoped>
.main-banner {
  padding: 2rem 1.5rem;
  max-width: 1200px;
  margin: auto;
}

/* Top Banner */
.top-banner {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  margin-bottom: 2rem;
}

.slogan {
  flex: 3;
}

.slogan h1 {
  font-size: 3rem;
  font-weight: bold;
  line-height: 1.2;
  color: #2c3e50;
}

.reviews {
  flex: 2;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.review-text {
  font-size: 1.1rem;
  margin-bottom: 1rem;
  color: #555;
}

.user-info {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.user-images img {
  width: 40px;
  height: 40px;
  object-fit: cover;
  border-radius: 50%;
  border: 2px solid #fff;
  margin-left: -10px;
}

.user-images img:first-child {
  margin-left: 0;
}

.user-count {
  font-weight: 600;
  color: #2c3e50;
}

/* Image Grid */
.image-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

/* Left side */
.left-block {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  min-width: 0;
}

.top-img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  border-radius: 8px;
}

.bottom-row {
  display: flex;
  gap: 1rem;
}

.bottom-row img {
  flex: 1;
  height: 250px;
  width: 45%;
  object-fit: cover;
  border-radius: 8px;
}

/* Right side */
.right-block {
  flex: 1;
  min-width: 0;
}

.right-block img {
  width: 100%;
  height: 520px;
  object-fit: cover;
  border-radius: 8px;
}

/* Mobile view */
@media (max-width: 768px) {
  .top-banner {
    flex-direction: column;
  }

  .image-grid {
    flex-direction: column;
  }

  .top-img,
  .bottom-row img,
  .right-block img {
    width: 100%;
    height: auto;
  }

  .bottom-row {
    flex-direction: column;
  }
}
</style>
