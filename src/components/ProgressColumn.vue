<script setup>
const props = defineProps({
	name: {
		type: String,
		required: true,
	},
	progress: {
		type: Number,
		required: true,
		validator: (value) => value >= 0 && value <= 100,
	},
	class_column: {
		type: String,
		required: true,
	},
	class_progress: {
		type: String,
		required: true,
	},
});

const colClasses = `vertical-progress-bar ${props.class_column}`;
const progressClasses = `fill ${props.class_progress}`;
</script>

<template>
	<div :class="colClasses" :title="name">
		<div :class="progressClasses" :style="{ height: `${progress}%` }"></div>
	</div>
</template>

<style scoped>
.vertical-progress-bar {
	position: relative;
}

.fill {
	width: 100%;
	position: absolute;
	bottom: 0;
	transition: height 0.5s ease; /* Add transition for smooth height changes */
}
</style>
