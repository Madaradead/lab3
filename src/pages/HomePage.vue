<template>
  <div class="home-page">
    <h1>Вітаємо у нашому SPA!</h1>
    <p>
      Це простий  застосунок , 
      створений за допомогою Vue 3, Vite та Vue Router.
    </p>
    <p>
      Перейдіть до <router-link to="/items">Каталогу</router-link>, 
      щоб побачити список посилань.
    </p>
  </div>
</template>

<script setup>
</script>

<style scoped>
.home-page {
  text-align: center;
}
h1 {
  color: #42b883;
}
p {
  font-size: 1.1rem;
  line-height: 1.6;
}
p a {
  color: #42b883;
  font-weight: bold;
  text-decoration: none;
}
p a:hover {
  text-decoration: underline;
}
</style>