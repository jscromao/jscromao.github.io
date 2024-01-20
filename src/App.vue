<script setup>
//import { RouterLink, RouterView } from "vue-router";
import { RouterView } from "vue-router";
</script>

<template>
	<div
		class="flex flex-col gap-x-2 px-2 py-1 items-center justify-center fixed top-2 right-2 bg-slate-900/90 border rounded-md text-xs text-slate-100 opacity-[.6] text-opacity-80 z-[90] scale-90"
	>
		<div class="w-full flex flex-row items-center justify-center text-nowrap whitespace-nowrap">Made With</div>
		<div class="flex flex-row gap-x-1 p-0 items-center justify-center">
			<a class="inline-flex flex-row gap-x-1" href="https://vuejs.org/" target="_blank" rel="noopener">
				<svg class="logo" viewBox="0 0 128 128" width="24" height="24">
					<path fill="#42b883" d="M78.8,10L64,35.4L49.2,10H0l64,110l64-110C128,10,78.8,10,78.8,10z"></path>
					<path fill="#35495e" d="M78.8,10L64,35.4L49.2,10H25.6L64,76l38.4-66H78.8z"></path>
				</svg>
				<span class="text hidden">Vue.js</span>
			</a>
			<a class="inline-flex flex-row gap-x-1" href="https://tailwindcss.com/" target="_blank" rel="noopener">
				<svg viewBox="0 0 52 31" class="text-slate-900 dark:text-white w-auto h-5">
					<path
						fill-rule="evenodd"
						clip-rule="evenodd"
						d="M25.517 0C18.712 0 14.46 3.382 12.758 10.146c2.552-3.382 5.529-4.65 8.931-3.805 1.941.482 3.329 1.882 4.864 3.432 2.502 2.524 5.398 5.445 11.722 5.445 6.804 0 11.057-3.382 12.758-10.145-2.551 3.382-5.528 4.65-8.93 3.804-1.942-.482-3.33-1.882-4.865-3.431C34.736 2.92 31.841 0 25.517 0zM12.758 15.218C5.954 15.218 1.701 18.6 0 25.364c2.552-3.382 5.529-4.65 8.93-3.805 1.942.482 3.33 1.882 4.865 3.432 2.502 2.524 5.397 5.445 11.722 5.445 6.804 0 11.057-3.381 12.758-10.145-2.552 3.382-5.529 4.65-8.931 3.805-1.941-.483-3.329-1.883-4.864-3.432-2.502-2.524-5.398-5.446-11.722-5.446z"
						fill="#38bdf8"
					></path>
				</svg>
				<span class="text hidden">Tailwind.css</span>
			</a>
			<a href="https://fontawesome.com/" target="_blank" rel="noopener">
				<svg viewBox="0 0 16 16" shape-rendering="geometricPrecision" text-rendering="geometricPrecision" class="w-[1.18rem]">
					<g clip-path="url(#logo-flag-animated-mask-clip-path)">
						<g transform="translate(11.3,7)" class="logo-flag-animated-flag-wave-to">
							<path
								d="M11.25,2.5c.9875,0,1.6438-.25,2.3-.5s1.3125-.5,2.3001-.5c.9873,0,1.6624.25,2.3374.5l.0491.01824C18.8946,2.26203,19.5368,2.5,20.5,2.5c.9875,0,1.6438-.25,2.3-.5s1.3125-.5,2.3001-.5c.9873,0,1.6624.25,2.3374.5l.0491.01824c.658.24379,1.3002.48176,2.2634.48176.9875,0,1.6438-.25,2.3-.5.6563-.25,1.3125-.5,2.3001-.5.9873,0,1.6624.25,2.3374.5l.0491.01824C37.3946,2.26203,38.0368,2.5,39,2.5v2c-.9666,0-1.616-.23962-2.2791-.48438l-.049-.01794C35.9958,3.74841,35.322,3.5,34.3501,3.5c-.9876,0-1.6438.25-2.3001.5-.6562.25-1.3125.5-2.3.5-.9666,0-1.6161-.23963-2.2791-.48422-.0163-.00603-.0327-.01207-.049-.0181C26.7458,3.74841,26.072,3.5,25.1001,3.5c-.9876,0-1.6438.25-2.3001.5s-1.3125.5-2.3.5c-.9666,0-1.616-.23962-2.2791-.48438l-.049-.01794C17.4958,3.74841,16.822,3.5,15.8501,3.5c-.9876,0-1.6438.25-2.3001.5s-1.3125.5-2.3.5c-.9666,0-1.61597-.23962-2.27905-.48438l-.04907-.01794C8.24585,3.74841,7.57202,3.5,6.6001,3.5c-.98755,0-1.6438.25-2.30005.5s-1.3125.5-2.30005.5v-2c.98755,0,1.6438-.25,2.30005-.5s1.3125-.5,2.30005-.5c.9873,0,1.66235.25,2.3374.5l.04834.01794C9.64377,2.26174,10.2868,2.5,11.25,2.5Zm0,8c.9875,0,1.6438-.25,2.3-.5s1.3125-.5,2.3001-.5c.9873,0,1.6624.25,2.3374.5l.0491.0182c.658.2438,1.3002.4818,2.2634.4818.9875,0,1.6438-.25,2.3-.5s1.3125-.5,2.3001-.5c.9873,0,1.6624.25,2.3374.5l.0491.0182c.658.2438,1.3002.4818,2.2634.4818.9875,0,1.6438-.25,2.3-.5.6563-.25,1.3125-.5,2.3001-.5.9873,0,1.6624.25,2.3374.5l.0491.0182c.658.2438,1.3002.4818,2.2634.4818v2c-.9666,0-1.616-.2396-2.2791-.4844l-.049-.0179c-.6761-.2493-1.3499-.4977-2.3218-.4977-.9876,0-1.6438.25-2.3001.5-.6562.25-1.3125.5-2.3.5-.9666,0-1.6161-.2396-2.2791-.4842-.0163-.0061-.0327-.0121-.049-.0181-.6761-.2493-1.3499-.4977-2.3218-.4977-.9876,0-1.6438.25-2.3001.5s-1.3125.5-2.3.5c-.9666,0-1.616-.2396-2.2791-.4844l-.049-.0179c-.6761-.2493-1.3499-.4977-2.3218-.4977-.9876,0-1.6438.25-2.3001.5s-1.3125.5-2.3.5c-.9666,0-1.61597-.2396-2.27905-.4844l-.04907-.0179C8.24585,11.7484,7.57202,11.5,6.6001,11.5c-.98755,0-1.6438.25-2.30005.5s-1.3125.5-2.30005.5v-2c.98755,0,1.6438-.25,2.30005-.5s1.3125-.5,2.30005-.5c.9873,0,1.66235.25,2.3374.5l.04834.0179c.65793.2438,1.30096.4821,2.26416.4821Z"
								transform="translate(-20.5,-7)"
								fill="#538dd7"
							></path>
						</g>
						<rect width="2" height="8" rx="0" ry="0" transform="translate(13 3)" fill="#538dd7"></rect>
						<path
							d="M0,16h16v-16L0,0v16ZM2,1q.075195.556641,0,7h3v7h10v-14L2,1Z"
							clip-rule="evenodd"
							fill="transparent"
							fill-rule="evenodd"
						></path>
						<clipPath id="logo-flag-animated-mask-clip-path">
							<rect width="16" height="16" rx="0" ry="0" fill="#000"></rect>
						</clipPath>
					</g>
					<path
						d="M2,1c-.55228,0-1,.44772-1,1v12c0,.5523.44772,1,1,1s1-.4477,1-1L3,2c0-.55228-.44772-1-1-1Z"
						fill="#000080"
					></path>
				</svg>
			</a>
		</div>
	</div>

	<div class="flex flex-col w-full">
		<nav
			id="topnav"
			ref="topnavRef"
			class="w-full bg-green-800 dark:bg-green-800 text-gray-100 font-semibold px-0 z-30 justify-between items-center shadow-lg sticky top-0 backdrop-blur transition duration-150 ease-in-out flex flex-row -translate-y-0 md:-translate-y-full md:-mt-14 subheading text-md h-14 py-2"
		>
			<div class="flex flex-row items-center gap-x-2 w-full px-4">
				<div class="flex h-full items-center hover:bg-black/[.0]">
					<img
						alt="José Romão"
						src="/profile.jpg"
						class="w-8 aspect-square rounded-full outline outline-offset-2 outline-2 outline-green-300/[.95]"
					/>
				</div>
				<div
					class="flex flex-row flex-grow gap-x-2.5 h-full items-center [&>a]:flex [&>a]:h-full [&>a]:items-center [&>a]:transition [&>a:hover]:text-green-200/[.9] [&>a:hover]:scale-105 [&>a:hover]:bg-black/[.0] flex-wrap md:flex-nowrap text-sm md:text-base justify-evenly"
				>
					<a :href="pdfPath" target="_blank" rel="noopener" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-file-pdf w-4 h-4"></i><span class="">Resume</span>
					</a>
					<a href="#profile" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-id-card-clip w-4 h-4"></i>
						<span>Contacts</span>
					</a>
					<a href="#traits" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-list-check w-4 h-4"></i>
						<span>Traits</span>
					</a>
					<a href="#skills" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-code w-4 h-4"></i>
						<span>Skills</span>
					</a>
					<a href="#experience" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-briefcase w-4 h-4"></i>
						<span>Experience</span>
					</a>
					<a href="#education" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-graduation-cap w-4 h-4"></i>
						<span>Education</span>
					</a>
					<a href="#languages" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-language w-4 h-4"></i>
						<span>Languages</span>
					</a>
					<a href="#merits" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-medal w-4 h-4"></i>
						<span>Merits</span>
					</a>
					<a href="#interests" class="flex flex-row gap-x-1">
						<i class="fa-solid fa-seedling w-4 h-4"></i>
						<span>Interests</span>
					</a>
				</div>
			</div>
		</nav>

		<div class="flex flex-row subheading items-stretch">
			<nav
				id="sidenav"
				ref="sidenavRef"
				class="bg-green-800 dark:bg-green-800 text-gray-100 font-semibold w-max gap-y-2.5 pt-24 z-40 top-0 left-0 transition duration-150 ease-in-out flex flex-col self-stretch [&>*]:w-full md:delay-150 -translate-x-full md:-translate-x-0 text-xl px-[5%] flex-grow-0"
			>
				<div
					class="sticky top-24 flex flex-col gap-y-2 [&>a]:transition [&>a:hover]:text-green-200/[.9] [&>a:hover]:scale-105 [&>a:hover]:bg-black/[.0]"
				>
					<div class="!pointer-events-none mb-4 -translate-x-[5%]">
						<!--<img alt="Vue logo" class="!w-12 aspect-square" src="@/assets/logo.svg" />-->
						<img
							alt="José Romão"
							src="/profile.jpg"
							class="w-28 aspect-square rounded-full ring-4 ring-green-300/[.95] ring-offset-4 ring-offset-green-800"
						/>
					</div>
					<!--<a :href="pdfPath" :download="pdfName" class="flex flex-row gap-x-2">-->
					<a :href="pdfPath" target="_blank" rel="noopener" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-file-pdf h-6 w-6"></i><span class="">Resume</span>
					</a>
					<a href="#profile" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-id-card-clip w-6 h-6"></i>
						<span>Contacts</span>
					</a>
					<a href="#traits" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-list-check w-6 h-6"></i>
						<span>Traits</span>
					</a>
					<a href="#skills" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-code h-6 w-6"></i>
						<span>Skills</span>
					</a>
					<a href="#experience" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-briefcase h-6 w-6"></i>
						<span>Experience</span>
					</a>
					<a href="#education" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-graduation-cap w-6 h-6"></i>
						<span>Education</span>
					</a>
					<a href="#languages" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-language w-6 h-6"></i>
						<span>Languages</span>
					</a>
					<a href="#merits" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-medal w-6 h-6"></i>
						<span>Merits</span>
					</a>
					<a href="#interests" class="flex flex-row gap-x-2">
						<i class="fa-solid fa-seedling w-6 h-6"></i>
						<span>Interests</span>
					</a>
				</div>
			</nav>

			<div class="flex flex-col px-8 transition -translate-x-[15%] md:-translate-x-0 w-max">
				<!--md:translate-y-14 -->
				<RouterView class="z-80 bg-slate-200" />
			</div>
		</div>
	</div>
	<button
		id="sidenav-open"
		ref="sidenavOpenRef"
		class="float-end flex px-1 py-1.5 rounded bg-green-800 dark:bg-green-900 text-gray-100 font-semibold z-50 justify-center items-center aspect-square h-8 shadow-lg sticky top-0.5 left-0.5 backdrop-blur !hidden"
		@click="handleSidenavTrigger"
	>
		<i class="fa-solid fa-bars"></i>
	</button>
</template>

<script>
let pdfName = "Resume_Jose_Romao.pdf";
export default {
	data() {
		return {
			pdfPath: pdfName, //: process.env.BASE_URL + 'resume.pdf',
		};
	},
	mount() {
		//const sidenav = this.$refs.sidenavRef;
		//sidenav.classList.remove("invisible");
		//sidenav.classList.add("transition");
	},
	mounted() {
		// Dynamically add the Font Awesome script to the head
		const script = document.createElement("script");
		script.src = "https://use.fontawesome.com/releases/v6.3.0/js/all.js";
		script.crossOrigin = "anonymous";
		script.async = true;
		document.head.appendChild(script);
	},
	methods: {
		handleSidenavTrigger(event) {
			//const sidenav = this.$refs.sidenavRef;
			//sidenav.classList.toggle("-translate-x-full");
			event.preventDefault();
		},
	},
};
</script>

<style scoped>
body,
body * {
	font-family:
		"Muli",
		-apple-system,
		BlinkMacSystemFont,
		"Segoe UI",
		Roboto,
		"Helvetica Neue",
		Arial,
		sans-serif,
		"Apple Color Emoji",
		"Segoe UI Emoji",
		"Segoe UI Symbol",
		"Noto Color Emoji";
}

.heading,
.heading *,
.subheading,
.subheading * {
	font-family:
		"Saira Extra Condensed",
		-apple-system,
		BlinkMacSystemFont,
		"Segoe UI",
		Roboto,
		"Helvetica Neue",
		Arial,
		sans-serif,
		"Apple Color Emoji",
		"Segoe UI Emoji",
		"Segoe UI Symbol",
		"Noto Color Emoji";
}
</style>
