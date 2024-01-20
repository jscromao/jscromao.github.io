<script setup>
const props = defineProps({
	lang: {
		type: String,
		required: true,
	},
	level: {
		type: Number,
		required: true,
		validator: (val) => val >= 20,
	},
	extrainfo: {
		type: String,
		required: false,
	},
	inList: {
		type: Boolean,
		required: false,
	},
	class: {
		type: String,
		required: false,
	},
});
const hasExtra = props.extrainfo !== undefined;
console.log("hasExtra: ", hasExtra);
const appliedClass = props.class ?? "";
const inList = !!props.inList;
console.log("inList: ", inList);

const textLevel =
	props.level >= 95
		? "C2"
		: props.level >= 80
			? "C1"
			: props.level >= 66
				? "B2"
				: props.level >= 50
					? "B1"
					: props.level >= 40
						? "A2"
						: props.level >= 20
							? "A1"
							: "None";

console.log(props.level, textLevel);
</script>

<template>
	<li v-if="inList" :title="lang" :class="appliedClass">
		<span class="fa-li"><i class="fas fa-check"></i></span>
		<strong>{{ lang }}</strong
		>, <span>{{ textLevel }}</span
		>&nbsp;<span v-if="hasExtra">({{ extrainfo }})</span>
	</li>
	<div v-else :class="appliedClass">
		<span class="fa-li"><i class="fas fa-check"></i></span>
		<strong>{{ lang }}</strong
		>, <span>{{ textLevel }}</span
		>&nbsp;<span v-if="hasExtra">({{ extrainfo }})</span>
	</div>
</template>
