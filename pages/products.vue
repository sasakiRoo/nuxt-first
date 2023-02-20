<script setup>
import ArticleCard from '../components/ArticleCard.vue'
const url = 'https://fakestoreapi.com/products/'
const { data: products } = useFetch(url)
</script>
<template>
    <h1 class="pt-10">all products</h1>
    <div class="parent-cards" v-for="data in products">
        <ArticleCard :title="data.title" :price="data.price" :descr="data.description" :id="data.id" />
    </div>
</template>
<style scoped>
.parent-cards {

    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(5, 1fr);
    grid-column-gap: 5px;
    grid-row-gap: 5px;

}
</style>