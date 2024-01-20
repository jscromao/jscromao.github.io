<script setup>
const props = defineProps({
	timeline: {
		type: String,
		required: true,
	},

	subject: {
		type: String,
		required: true,
	},

	entity: {
		type: String,
		required: true,
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
</script>

<template>
	<li v-if="inList" :title="lang" :class="appliedClass">
		<span class="fa-li"><i class="fas fa-scroll"></i></span>
		<span>{{ subject }}</span> - <span>{{ entity }}</span> - (<span>{{ timeline }}</span
		>)
		<span v-if="hasExtra" class="block">({{ extrainfo }})</span>
	</li>
	<div v-else :class="appliedClass">
		<span class="fa-li"><i class="fas fa-scroll"></i></span>
		<span>{{ subject }}</span> - <span>{{ entity }}</span> - (<span>{{ timeline }}</span
		>)
		<span v-if="hasExtra" class="block">({{ extrainfo }})</span>
	</div>
</template>
