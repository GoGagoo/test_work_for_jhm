<script setup>
import { ref } from 'vue'

const props = defineProps({
	color: {
		type: String,
		default: 'gray',
	},
})

const isBlue = ref(props.color === 'blue')
const isGreen = ref(props.color === 'green')
</script>

<template>
	<button
		class="transition ease-linear delay-100 mt-10  w-80 rounded-sm text-white text-center py-2"
		:class="{ 'button-blue': isBlue, 'button-green': isGreen }"
	>
	<slot />
	</button>
</template>
