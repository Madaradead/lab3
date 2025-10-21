<template>
  <div class="main-layout">
    <AppHeader />
    
    <main class="content">
      <router-view />
    </main>

    <AppFooter />
  </div>
</template>

<script setup>
// Імпортуємо компоненти хедера та футера
import AppHeader from '../components/AppHeader.vue'
import AppFooter from '../components/AppFooter.vue'
</script>

<style scoped>
.main-layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* Робить лейаут на всю висоту екрану */
}
.content {
  flex: 1; /* Змушує контент зайняти весь простір між хедером і футером */
  max-width: 960px;
  margin: 0 auto;
  padding: 2rem;
  width: 100%;
}
</style>