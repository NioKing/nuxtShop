<template>
    <div class="container">
        <div class="products-card" v-for="p in products">
            <div class="image">
                <img :src="p.image" alt="product image" style="height: 250px; object-fit: scale-down;">
            </div>
            <div class="description">
                <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
                <span>Price: {{ p.price }} </span>
            </div>
        </div>  
    </div>
</template>

<style>
.container {
    display: flex; 
    justify-content: space-around;
    flex-wrap: wrap;
}

.products-card {
    margin: 25px;
    box-shadow: 0px 2px 1px -1px rgb(0 0 0 / 20%),
        0px 1px 1px 0px rgb(0 0 0 / 14%),
        0px 1px 3px 0px rgb(0 0 0 / 12%);
    background: rgb(247, 245, 245);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    width: 290px;
    text-align: center;
    padding: 25px;
    min-height: 400px;
}
.description {
    gap: 10px;
}


</style>

<script setup>
const {data: products} = await useFetch('https://fakestoreapi.com/products')
</script>
