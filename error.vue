<template>
    <div class="error">
        <div class="error-data">
            <h1>{{ error.statusCode }}</h1>
            <span>{{ error.message }}</span>
            <div class="btn">
                <button @click="handleError">Go back</button>
            </div>
        </div>
    </div>
</template>

<style>
.error {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    font-size: 2rem;
}

.error-data {
    display: flex;
    align-items: center;
    flex-direction: column;
    text-align: center;
    gap: 20px;
}
</style>

<script setup>
defineProps(['error'])

const handleError = () => clearError({ redirect: '/products' })
</script>