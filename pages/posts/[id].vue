<script setup>
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id
const { data: product } = useFetch(uri)
</script>

<template>
	<div class="pt-10 h-screen">
		<h1>{{ product.title }}</h1>
		<p>{{ product.description }}</p>
		<p>{{ product.price }}</p>
	</div>
</template>