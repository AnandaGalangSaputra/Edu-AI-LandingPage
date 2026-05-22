<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="app-container">
    <!-- Sticky Glassmorphic Navigation Bar -->
    <Navbar />

    <!-- Dynamic Routed Core View -->
    <main class="content-wrapper">
      <router-view />
    </main>

    <!-- Brand Footer -->
    <Footer />
  </div>
</template>

<style>
.app-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.content-wrapper {
  flex-grow: 1;
}

/* Ensure padding so fixed navbar doesn't cover top of other pages */
.other-view {
  padding-top: 5rem;
}
</style>
