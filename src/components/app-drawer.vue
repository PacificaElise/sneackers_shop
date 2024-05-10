<script setup>
import ArrowLeft from './arrow-left.vue'
import CartList from './cart-list.vue'
import AppDivider from './app-divider.vue'
</script>

<template>
  <div class="w-full h-full fixed top-0 left-0 z-10 bg-black bg-opacity-50" />
  <div class="w-96 h-full flex flex-col p-8 fixed top-0 right-0 z-20 bg-white overflow-auto">
    <div class="flex gap-4 items-center">
      <button class="cursor-pointer opacity-30 transition hover:opacity-100 hover:-translate-x-1">
        <arrow-left />
      </button>
      <h2 class="text-2xl font-bold">Корзина</h2>
    </div>

    <cart-list />

    <div class="flex flex-col gap-2">
      <div class="flex justify-between">
        <span>Итого:</span>
        <b>12 900 руб.</b>
      </div>
      <app-divider />
      <div class="flex justify-between">
        <span>Налог 5%:</span>
        <b>900 руб.</b>
      </div>
      <app-divider />
    </div>

    <button
      class="w-full mt-4 p-4 rounded-xl text-white bg-lime-500 transition hover:bg-lime-600 active:bg-lime-700 disabled:bg-slate-400"
    >
      Оформить заказ
    </button>
  </div>
</template>
