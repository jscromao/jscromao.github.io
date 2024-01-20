<script setup>
const props = defineProps({
	countrycode: {
		type: Number,
		required: true,
	},
	number: {
		type: Number,
		required: true,
		validator: (val) => val >= 100,
	},
});

const numberAsString = `${String(props.number)}`;
console.log(numberAsString.length);
const eachLen = Math.max(1, Math.floor(numberAsString.length / 3));
const firstPart = numberAsString.slice(0, eachLen);
const secondPart = numberAsString.slice(eachLen, eachLen * 2);
const thirdPart = numberAsString.slice(eachLen * 2);
</script>

<template>
	<span class="inline-flex flex-row gap-x-1">
		<span class="">+{{ countrycode }}</span>
		<span class="">{{ firstPart }}</span>
		<span>{{ secondPart }}</span>
		<span>{{ thirdPart }}</span>
	</span>
</template>
