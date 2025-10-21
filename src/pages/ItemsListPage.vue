<template>
  <div>
    <h1>Каталог посилань</h1>
    <ul class="item-list">
      <li v-for="item in itemList" :key="item.id">
        <router-link :to="`/items/${item.id}`">
          {{ item.title }}
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { items } from '../data/items.js'

const itemList = ref(items)
</script>

<style scoped>
.item-list {
  list-style: none;
  padding: 0;
}
.item-list li {
  background: #f9f9f9;
  border: 1px solid #eee;
  padding: 1rem;
  margin-bottom: 0.5rem;
  border-radius: 5px;
}
.item-list li a {
  text-decoration: none;
  color: #35495e;
  font-weight: bold;
  font-size: 1.2rem;
}
.item-list li a:hover {
  color: #42b883;
}
</style>