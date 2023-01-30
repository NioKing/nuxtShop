<template>
    <div class="container">
        <div class="product-card">
            <div class="description">
                <span style="font-size: 2rem;">{{ product.title }}</span>
                <span>{{ product.description }}</span>
            </div>
            <img :src="product.image" alt="product image">
        </div>
    </div>
</template>

<style>
.container {
    display: flex;
    align-items: center;
    /* height: calc(100vh - 60px); */
}

.product-card {
    display: flex;
    border-bottom: 1px solid grey;
    width: 600px;
    padding: 20px;
    gap: 30px;
    box-shadow: 0px 2px 1px -1px rgb(0 0 0 / 20%),
            0px 1px 1px 0px rgb(0 0 0 / 14%),
            0px 1px 3px 0px rgb(0 0 0 / 12%);
 }

 .description {
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
    gap: 25px;
 }

 img {
    width: 250px;
 }
</style>


<script setup>
const {id} = useRoute().params
const uri = `https://fakestoreapi.com/products/` + id
const {data: product} = await useFetch(uri)

</script>