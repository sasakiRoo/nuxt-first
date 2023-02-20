<script>
export default {
	props: {
		id: Number,
		title: String,
		price: Number,
		descr: String,
	}
}
</script>

<template>
	<div class="card bg-slate-200 my-2 w-64 p-2">
		<h1 class="font-semibold">{{ title }}</h1>
		<p class="h-48 overflow-hidden">{{ descr }}</p>
		<p class="text-green-800">${{ price }}</p>
		<NuxtLink :to="`posts/${id}`">
			<span class="underline text-blue-900">Read fully...</span>
		</NuxtLink>
	</div>
</template>