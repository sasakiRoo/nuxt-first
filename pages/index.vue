<script setup>
import ArticleCard from '../components/ArticleCard.vue'
</script>

<script>
export default {
	data() {
		return {
			renderData: '',
		}
	},
	methods: {
		async getProductData() {
			const res = await fetch('https://fakestoreapi.com/products')
			this.renderData = await res.json()
		}
	},
	mounted() {
		this.getProductData()
	}
}
</script>

<template>
  <div class="container-home h-screen pt-10 overflow-auto bg-slate-300">
    <h1>hello nuxt app!</h1>
    <main class="content overflow-auto">
    	<div class="flex flex-col items-center justify-evenly" v-for="data in renderData">
    		<ArticleCard :title="data.titile" :price="data.price" :descr="data.description" :id="data.id"/>
    	</div>
    </main>
  </div>
</template>

<!-- <style scoped>
	.container-home {
		overflow: hidden;
	}
</style>
 -->