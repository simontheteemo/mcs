<!-- App.vue -->
<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="app-container">
    <!-- Optional: Add a navigation header here -->
    <!-- <nav class="nav-header">
      <router-link to="/" class="nav-link">Home</router-link>
    </nav> -->

    <!-- Main content wrapper -->
    <div class="main-content">
      <RouterView />
    </div>

    <!-- Optional: Add a footer here -->
  </div>
</template>

<style>
/* Global styles */
:root {
  --max-width: 1200px;
  --padding-x: 1rem;
}

body {
  margin: 0;
  padding: 0;
  min-height: 100vh;
}

.app-container {
  width: max-content;
  min-height: 100vh;
  display: flex;
  justify-content: center; /* Center horizontally */
}

.nav-header {
  padding: 1rem var(--padding-x);
  background-color: #f8f9fa;
  display: flex;
  justify-content: center;
  border-bottom: 1px solid #eee;
}

.nav-link {
  color: #333;
  text-decoration: none;
  padding: 0.5rem 1rem;
}

.nav-link:hover {
  color: #666;
}

.main-content {
  width: 100%;
  max-width: 1200px; /* Or whatever maximum width you prefer */
  padding: 2rem; /* Add some padding on the sides */
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .main-content {
    padding: 1rem;
  }
}
</style>
