<script setup>
import { onMounted, watch, ref, reactive } from 'vue'
import axios from 'axios'
import AppHeader from './components/app-header.vue'
import AppCardList from './components/app-card-list.vue'
// import AppDrawer from './components/app-drawer.vue'
import AppSearch from './components/app-search.vue'
import AppSelect from './components/app-select.vue'

const items = ref([])

const filters = reactive({
  sortBy: 'title',
  searchQuery: ''
})

const fetchItems = async () => {
  try {
    const params = {
      sortBy: filters.sortBy
    }

    if (filters.searchQuery) {
      params.title = `*${filters.searchQuery}*`
    }

    const { data } = await axios.get('https://5ba1fbbe4fbe93cb.mokky.dev/items', { params })
    items.value = data
    console.log(items.value)
  } catch (error) {
    alert(error)
  }
}

const onChangeSelect = (event) => {
  filters.sortBy = event.target.value
}

const onChangeSearch = (event) => {
  filters.searchQuery = event.target.value
}

onMounted(fetchItems)

watch(filters, fetchItems)
</script>

<template>
  <!-- <app-drawer /> -->
  <div class="w-4/5 m-auto mt-14 bg-white rounded-xl shadow-xl">
    <app-header />
    <main class="p-10">
      <div class="flex justify-between items-center mb-10">
        <h1 class="text-3xl font-bold">Все кроссовки</h1>
        <div class="flex gap-4">
          <app-select @change="onChangeSelect" />
          <app-search :on-change-search="onChangeSearch" />
        </div>
      </div>

      <app-card-list :items="items" />
    </main>
  </div>
</template>

<style scoped></style>
