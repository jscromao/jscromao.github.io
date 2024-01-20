<script setup>
import PhoneNumber from "./PhoneNumber.vue";
const props = defineProps({
	first_name: {
		type: String,
		required: true,
	},
	last_name: {
		type: String,
		required: true,
	},
	location: {
		type: String,
		required: true,
	},
	phonecountry: {
		type: Number,
		required: true,
	},
	phonenumber: {
		type: Number,
		required: true,
		validator: (val) => val >= 100,
	},
	email: {
		type: String,
		required: true,
	},
});

const mailto = "mailto:" + props.email;
</script>

<template>
	<div class="flex flex-col">
		<h1 class="text-7xl uppercase font-bold">
			<span>{{ first_name }}</span>
			<br />
			<span class="text-8xl text-green-900/90">{{ last_name }}</span>
		</h1>
		<div class="subheading mb-5">
			<span>
				<i class="fa-solid fa-location-dot mr-1"></i>
				<span>{{ location }}</span>
			</span>
			&nbsp; | &nbsp;
			<span>
				<i class="fa-solid fa-at mr-1"></i>
				<a :href="mailto">{{ email }}</a>
			</span>
			&nbsp; | &nbsp;
			<span>
				<i class="fa-solid fa-phone mr-1"></i>
				<PhoneNumber :countrycode="phonecountry" :number="phonenumber" />
			</span>
		</div>

		<slot></slot>

		<slot name="socials"></slot>
	</div>
</template>
