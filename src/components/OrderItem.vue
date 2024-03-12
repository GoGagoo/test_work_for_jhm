<script>
import { defineProps } from 'vue'


defineProps({
	title: String,
	quantity: Number,
	price: Number,
})
</script>

<template>
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
</template>
