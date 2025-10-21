<template>
  <div>
    <div v-if="item" class="item-details">
      <h1>{{ item.title }}</h1>
      <p class="description">{{ item.description }}</p>
      
      <a :href="item.url" target="_blank" rel="noopener noreferrer" class="external-link">
        Перейти за посиланням &rarr;
      </a>

      <router-link to="/items" class="back-link">&larr; Назад до списку</router-link>
    </div>
    <div v-else class="not-found">
      <h2>Елемент не знайдено</h2>
      <router-link to="/items">Повернутись до каталогу</router-link>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import { items } from '../data/items.js'

const props = defineProps({
  id: {
    type: String,
    required: true
  }
})


const item = computed(() => {
  return items.find(i => i.id === parseInt(props.id))
})
</script>

<style scoped>
.item-details h1 {
  color: #42b883;
  border-bottom: 2px solid #f0f0f0;
  padding-bottom: 0.5rem;
}
.description {
  font-size: 1.1rem;
  line-height: 1.7;
  margin: 1.5rem 0;
}

.external-link {
  display: inline-block;
  padding: 10px 15px;
  background-color: #42b883;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  margin-bottom: 1.5rem;
  transition: background-color 0.3s;
}
.external-link:hover {
  background-color: #35495e;
}

.back-link {
  display: block; 
  color: #42b883;
  text-decoration: none;
  font-weight: bold;
}
.not-found {
  text-align: center;
  color: #e74c3c;
}
</style>