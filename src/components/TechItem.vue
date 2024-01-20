<script setup>
import ProgressColumn from "./ProgressColumn.vue";

const props = defineProps({
	tech: {
		type: String,
		required: true,
	},
	icon: {
		type: String,
		required: false,
	},
	recency: {
		type: Number,
		required: true,
		validator: (val) => val >= 0 && val <= 100,
	},
	proficiency: {
		type: Number,
		required: true,
		validator: (val) => val >= 0 && val <= 100,
	},
});
const hasIcon = props.icon !== undefined;
console.log(hasIcon);
console.log(props.icon);
</script>

<template>
	<!--<div class="flex flex-row gap-x-0.5 items-center justify-between h-18 aspect-square border rounded border-gray-500/50 p-0.5">-->
	<div class="grid grid-cols-7 gap-x-0.5 items-center justify-between h-18 aspect-square border rounded border-gray-500/50 p-0.5">
		<!--<div class="inline-block border rounded border-gray-500/50 p-1 h-full aspect-square">-->
		<div class="h-full w-full flex items-center justify-center">
			<ProgressColumn
				:progress="recency"
				class_column="col-span-1 inline-block flex-grow-0 flex-shrink-0 w-1/2 h-full bg-gray-800 rounded-sm"
				class_progress="bg-emerald-400"
				name="Recency"
			/>
		</div>
		<div v-if="hasIcon" class="col-span-5 flex flex-row flex-1 h-full items-center justify-center text-2xl font-semibold w-full">
			<i :title="tech" :class="`fab ${icon} w-full aspect-square h-auto`"></i>
		</div>
		<div v-else class="col-span-5 flex flex-col h-full items-center justify-center align-middle text-2xl font-semibold w-full">
			<div class="inline-flex flex-row h-fit items-start justify-center text-2xl font-semibold">
				<span>{{ tech }}</span>
			</div>
		</div>
		<div class="h-full flex items-center justify-center">
			<ProgressColumn
				:progress="proficiency"
				class_column="col-span-1 inline-block flex-grow-0 flex-shrink-0 w-1/2 h-full bg-gray-800 rounded-sm"
				class_progress="bg-blue-400"
				name="Proficiency"
			/>
		</div>
		<!--<span>{{ proficiency }}%</span>-->
		<!--</div>-->
	</div>
</template>
