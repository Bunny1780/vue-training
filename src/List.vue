<script setup>
defineProps(["products"])
</script>

<template>
    <ul v-for="product in products">
        <li>Name : {{ product.name }}</li>
        <li>Price : {{ product.price }}</li>
        <li>Note : {{ product.description }}</li>
    </ul>
</template>

<style scoped>
</style>