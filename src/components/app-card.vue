<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function
})
</script>

<template>
  <div
    class="p-6 relative border-slate-100 rounded-2xl bg-white cursor-pointer transition hover:-translate-y-2 hover:shadow-xl"
  >
    <button class="absolute top-8 left-8" @click="onClickFavorite">
      <img :src="isFavorite ? '/like-2.svg' : '/like-1.svg'" alt="favorite" />
    </button>
    <img :src="imageUrl" alt="sneaker" />

    <p class="mt-2">{{ title }}</p>
    <div class="mt-5 flex justify-between items-end">
      <div class="flex flex-col">
        <span class="text-slate-400 uppercase">Цена:</span>
        <span class="font-bold">{{ price }} руб.</span>
      </div>
      <button @click="onClickAdd">
        <img :src="isAdded ? '/checked.svg' : '/plus.svg'" alt="add" />
      </button>
    </div>
  </div>
</template>
