<template>
    <nav class="navbar">
        <div class="nav-title">
            <NuxtLink to="/" style="text-decoration: none;">Store App</NuxtLink>
        </div>
        <div class="links">
            <NuxtLink class="link" to="/products">Store</NuxtLink>
            <NuxtLink class="link" to="/cart">Cart</NuxtLink>
            <NuxtLink class="link" to="/about">About us</NuxtLink>
            <NuxtLink class="link" to="/contacts">Contacts</NuxtLink>
        </div>
    </nav>
    <slot />
</template>

<style>
nav {
    background: aqua;
    display: flex;
    gap: 15px;
    height: 60px;
    align-items: center;
    font-size: 1.5rem;
    padding-left: 20px;
    padding-right: 20px;
    justify-content: space-between;
}

.title {
    cursor: pointer;
}

.links {
    display: flex;
    gap: 20px;
}

.router-link-active {
    color: black;
}

.router-link-exact-active {
    color: black;
}

.link {
    text-decoration: none;
}
</style>

<script setup>


</script>