<script setup lang="ts">
import HeaderBlock from '../src/components/HeaderBlock.vue';
</script>

<template>
	<div class="flex flex-col min-h-screen bg-background">
		<HeaderBlock />
		<main class="container mx-auto p-3 flex-grow mb-12">
			<slot />
		</main>
	</div>
</template>
