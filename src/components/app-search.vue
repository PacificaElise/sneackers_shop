<script setup>
defineProps({
  onChangeSearch: Function
})
</script>

<template>
  <div class="relative">
    <img src="/search.svg" alt="search" class="absolute top-1/2 left-3 -translate-y-1/2" />
    <input
      @input="onChangeSearch"
      type="text"
      placeholder="Поиск..."
      class="py-2 pl-10 pr-3 border border-slate-200 rounded-md outline-none focus:border-slate-400"
    />
  </div>
</template>
