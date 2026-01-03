<script setup lang="ts">
import Block from '../../src/components/Block.vue';
import PageTitle from '../../src/components/PageTitle.vue';
import SkillBubble from '../../src/components/SkillBubble.vue';
import { skills } from '../../src/data/skill';
</script>

<template>
	<PageTitle icon="file" title="Резюме" />
	<Block>
		<h2>Навыки</h2>
		<div class="flex gap-2 flex-wrap">
			<SkillBubble
				v-for="skill in skills"
				:key="skill.id"
				:id="skill.id"
			/>
		</div>
	</Block>
</template>
