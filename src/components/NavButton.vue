<script setup lang="ts">
import Svg from './Svg.vue';

const props = defineProps({
	to: {
		type: String,
		required: true,
	},
	text: {
		type: String,
		required: false,
	},
	iconName: {
		type: String,
		required: false,
	},
	iconSize: {
		type: [String, Number],
		required: false,
		default: 16,
	},
});
</script>

<template>
	<NuxtLink
		:to="to"
		class="flex items-center font-medium text-text-primary text-lg hover:text-blue-600 transition duration-200 group"
	>
		<Svg
			v-if="iconName"
			:icon="iconName"
			:size="Number(iconSize)"
			class="mr-1 fill-text-primary group-hover:fill-blue-600 transition duration-200"
		></Svg>
		<span>{{ text }}</span>
	</NuxtLink>
</template>
