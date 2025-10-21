<template>
  <header class="app-header">
    <div class="logo">Мій SPA</div>
    <nav>
      <router-link to="/">Головна</router-link>
      <router-link to="/items">Каталог</router-link>
    </nav>
  </header>
</template>

<script setup>
// Скрипти не потрібні
</script>

<style scoped>
.app-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: #35495e;
  color: white;
}
.logo {
  font-size: 1.5rem;
  font-weight: bold;
}
nav a {
  color: white;
  text-decoration: none;
  margin-left: 1.5rem;
  font-size: 1.1rem;
}
nav a:hover,
.router-link-active { 
  /* vue-router автоматично додає цей клас активному посиланню */
  color: #42b883;
  text-decoration: underline;
}
</style>