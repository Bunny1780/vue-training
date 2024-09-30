<script setup>
defineProps(["products"])
</script>

<template>
    <div v-for="product in products">
        <h3>{{ product.name }}</h3>
        <p>{{ product.price }}</p>
        <p>{{ product.description }}</p>
    </div>
</template>

<style scoped>
</style>