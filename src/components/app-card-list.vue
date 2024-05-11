<script setup>
import AppCard from './app-card.vue'

defineProps({
  items: Array
})
</script>

<template>
  <div class="grid grid-cols-4 gap-4">
    <app-card
      v-for="item in items"
      :key="item.id"
      :title="item.title"
      :imageUrl="item.imageUrl"
      :price="item.price"
      :isFavorite="item.isFavorite"
      :isAdded="item.isAdded"
    />
  </div>
</template>
