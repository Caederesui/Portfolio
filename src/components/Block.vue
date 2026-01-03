<script setup lang="ts">
import { computed } from 'vue';

const props = defineProps<{
	isLink?: boolean;
}>();

const blockClasses = computed(() => {
	const baseClasses = 'bg-block rounded-2xl shadow-2xl p-10';
	if (props.isLink) {
		return `${baseClasses} cursor-pointer transition duration-300 ease-in-out hover:bg-block`;
	}
	return baseClasses;
});
</script>

<template>
	<div :class="blockClasses">
		<slot></slot>
	</div>
</template>
