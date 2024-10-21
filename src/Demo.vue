<script setup>
    import { ref } from 'vue';
    let message = ref('Hello world!');
</script>

<template>
    <h1>{{ message }}</h1>
    <input v-model="message">
    <h2>Test</h2>
</template>

<style scoped>
</style>