<template>
    <nav>
        <div class="title">
            <NuxtLink to="/">Store App</NuxtLink>
        </div>
        <div class="links">
            <NuxtLink to="/">About us</NuxtLink>
            <NuxtLink to="/">Store</NuxtLink>
            <NuxtLink to="/">Contacts</NuxtLink>
        </div>
    </nav>
    <slot/>
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
        text-decoration: none;
        color: black;
    }

    .router-link-exact-active {
        color: black
    }
</style>

<script setup>


</script>