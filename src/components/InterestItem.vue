<template>
	<div class="flex flex-col">
		<h3 class="subheading text-3xl text-slate-900/80 font-bold">
			<slot name="icon"></slot>
			&nbsp;
			<slot name="interest"></slot>
		</h3>
		<div class="mt-1.5 text-lg">
			<slot name="description"></slot>
		</div>
	</div>
</template>
