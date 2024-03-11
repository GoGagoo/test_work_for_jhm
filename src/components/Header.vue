<script setup>
import Button from './Button.vue'
import Order from './Order.vue'

</script>

<template>
	<div class="flex flex-col pt-9 bg-neutral-200">
		<div class="grid grid-rows-1 grid-flow-col gap-4">
			<div class="row-span-3">
				<Order />
			</div>

			<div class="col-span-12 pt-12 mr-12">
				<div>
					
				</div>
				<table class="w-full table-auto overflow-scroll max-h-32">
					<thead>
						<tr>
							<th class="px-4 text-blue-600 py-2 font-light text-left text-xl">
								Название товара
							</th>
							<th class="px-4 text-blue-600 py-2 font-light text-right text-xl">
								Количество
							</th>
							<th class="px-1 py-2 text-blue-600 font-light text-right text-xl">
								Стоимость
							</th>
						</tr>
					</thead>
					<tbody class="overflow-y-scroll">
						<tr>
							<td class="px-4 py-3 font-light">Борщевой набор номер три</td>
							<td class="px-4 py-2 text-right">
								<input
									value="11 шт."
									class="w-12 bg-transparent font-light text-center"
								/>
							</td>
							<td class="px-4 py-2 text-right font-light border-gray-300">
								1100.00
							</td>
						</tr>
						
					</tbody>
				</table>
			</div>


			<div class="row-span-2 col-span-12 mt-12">
				<div class="rounded-lg p-4">
					<h2 class="text-lg text-right mr-12 mb-2">Итого: 3400</h2>
				</div>
				<Button class="p-12 mt-2 ml-96" color="green">
						Сохранить
					</Button>
			</div>
		</div>
	</div>
</template>
