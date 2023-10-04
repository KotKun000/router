<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import Button from './components/Button.vue'
</script>

<template>
  <header>

    <div class="container">
      <div class="logo">
        <h1>Cafe ☕</h1>
      </div>
      <div class="con-item">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/review">Review</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </div>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 200px 1fr;
  color: azure;
  background-color: rgb(100, 91, 70);
  padding: 10px;
}

.con-item {
  display: flex;
  gap: 20px;
  align-items: center;
}

.con-item a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

.con-item a:hover {
  text-decoration: underline;
}
</style>