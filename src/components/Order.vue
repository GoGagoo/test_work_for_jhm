<script setup>
import AddButton from './AddButton.vue'
import { ref, onMounted } from 'vue'

const products = ref([])

onMounted(async () => {
  const response = await fetch('https://dev-su.eda1.ru/test_task/products.php')
  const data = await response.json()
  products.value = data.products
})
</script>

<template>
	<header class="pl-6">
		<div class="flex justify-between items-center">
			<h1 class="text-xl font-light">Выберите продукцию</h1>
		</div>
	</header>

	<div class="pt-5 w-50 border-b-blue-400">
		<select
			class="ml-6 pl-4 py-3 pr-8 border border-black focus:outline-none font-light text-left w-80 bg-[#EEF8FF] border-b-blue-400 sm:text-xl text-blue-400 rounded-none"
		>
			<option>Выберите продукцию</option>
			<option v-for="product in products" :key="product.id">{{ product.title }}</option>
		</select>
	</div>

	<div class="pt-9 bg-neutral-200">
		<header class="pl-6">
			<div class="flex justify-between items-center">
				<h1 class="text-xl font-light">Введите количество</h1>
			</div>
		</header>
	</div>

	<div class="pt-5 pl-6">
		<input
			class="text-xl w-80 py-3 pl-4 text-blue-400 border border-b-blue-400 focus:outline-none bg-[#EEF8FF]"
			placeholder="0"
			type="number"
			min="0"
		/>
	</div>

	<AddButton />
</template>
