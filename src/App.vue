<script setup>
import AppHeader from './components/app-header.vue'
import AppCardList from './components/app-card-list.vue'
// import AppDrawer from './components/app-drawer.vue'
import AppSearch from './components/app-search.vue'
import AppSelect from './components/app-select.vue'
</script>

<template>
  <!-- <app-drawer /> -->
  <div class="w-4/5 m-auto mt-14 bg-white rounded-xl shadow-xl">
    <app-header />
    <main class="p-10">
      <div class="flex justify-between items-center mb-5">
        <h1 class="text-3xl font-bold">Все кроссовки</h1>
        <div class="flex gap-4"><app-select /> <app-search /></div>
      </div>

      <app-card-list />
    </main>
  </div>
</template>

<style scoped></style>
