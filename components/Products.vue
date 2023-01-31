<template>
    <div class="container">
        <div class="products-card" v-for="p in products">
            <div class="image">
                <img :src="p.image" alt="product image" style="height: 250px; object-fit: scale-down;">
            </div>
            <div class="description">
                <NuxtLink class="title" :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
                <span style="font-size: 1.25rem;">Price: {{ p.price }} </span>
                <div class="btn">
                    <button>Add to cart</button>
                </div>
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
    width: 300px;
    text-align: center;
    padding: 25px;
    min-height: 480px;
}

.description {
    padding: 10px;
    gap: 10px;
}

.btn {
    display: flex;
    justify-content: center;
}
.btn > button {
    min-width: 100px;
    min-height: 40px;
    font-size: 1.1rem;
    padding: 10px;
    border: none;
    border-radius: 6px;
    box-shadow: 0px 3px 5px 0px rgb(0 0 0 / 20%),
            0px 2px 3px 0px rgb(0 0 0 / 14%),
            0px 2px 3px 0px rgb(0 0 0 / 12%);
    cursor: pointer;
}

.btn :hover {
    background: rgba(230, 230, 230, 0.8);
}

.btn :active {
    background: rgba(200, 200, 200, 0.8);
}
.title {
    text-decoration: none;
    font-size: 1.25rem;
}

</style>

<script setup>
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>
